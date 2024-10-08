
- [[p.hasURL]] https://wiki.c2.com/?ActorVsAgent
- [[p.excerptedFrom]] [[book.efficient-node-js-a-beyond-the-basics-guide]]
- [[p.hasTopic]] [[t.cs.actors]] [[t.cs.agents]]

## [[p.hadContent]]


Actor Vs Agent
An 'Actor' from ActorsModel is similar to objects in OOP:

  passive between processing messages; presence of object in system is irrelevant unless hooked into a framework that will send messages to it
    communicate to an actor by sending a message to it; you must know the actor exists
    while processing a message, an actor may send more messages, create more actors, or update local state
    actors that need extra information in order to complete a task must store it locally or gather it via messages with replies
    actors tend to process inputs one at a time, and thus need to coordinate permutations
    actors using replies must wait upon them; without discipline, this can result in cyclic waits.

An 'Agent', as from ConcurrentConstraintProgramming or ReactiveDemandProgramming, is different:

  active continuously - making observations on an environment, constraint store, or perhaps other agents
    presence of agent may also affect the system, i.e. applying a rule or demand; nature of effect distinguishes Agent systems
    communicate to an agent by modifying something that it is observing; you do not need to know that the agent exists
    upon observing certain conditions, in some systems agents might spawn new agents or update local state
    the information that agents need to perform their jobs is continuously maintained by their runtime environment
    agents tend to process all relevant information at once, and thus need consider only combinations
    it takes some discipline to prevent 'feedback' systems, similar to placing a microphone near a speaker

They also share a number of similarities: concurrency, TuringComplete.

One can emulate Agents using Actors, but doing so requires a lot of framework and complexity. In particular, in Agent systems the specification of what data the framework must provide to a given agent is implicit in the source-code - and is easily subject to ad-hoc queries and calculations to allow different 'views' of the system. When emulating agents with actors, this information must usually be represented twice (once in the source code, once to hook the framework) and is often subject to a rigid view (though some systems do support flexible scripting languages to gather the data; at least one supports ad-hoc distributed SQL). These frameworks that allow us to treat Actors as Agents are often called PublishSubscribeModels. A standardized pubsub model is DataDistributionService by ObjectModelingGroup. Related is the ObserverPattern, TupleSpace, BlackboardMetaphor, ComplexEventProcessing.

It seems to me that, as far as SoftwareEngineering properties go, Agents are superior to Actors in every way. Agents are generally 'pluggable' - you can easily drop them onto a system, or just as easily pull them out; many are even hot-pluggable or subject to LiveProgramming, which allows a shorter edit-test-debug cycle. **Dealing with combinations of continuous inputs, rather than permutations of concurrent messages, dodges a great deal of complexity (roughly '2^N' instead of 'N!') without preventing agents from introducing a bit of ordering where critical.** Agents avoid a considerable amount of state associated with hooking into a system, cache management, and concurrency control (i.e. where Actors would require use of serializers).

A weakness of many agent systems is the use of a shared data space (tuple space, blackboard, constraint store) which raises many concurrency-control, authority, and confidentiality issues. Basically, with a central shared space, you must be very careful about inclusion of untrusted code. If one is not careful, it may also lead to a CentralPointOfFailure or a bottleneck, though those problems can be mitigated by distribution and replication of the space. But, if we reject a shared space, then we must answer: what do agents observe, how do agents affect the system, and how do we handle concurrency?   ^q42yd20t54qm

Hybrid Actor-Agent Models

If we want to avoid a common data-space, then one obvious possibility is that agents could observe one another.

To support security we don't allow agents unrestricted access to one another (since an agent might contain sensitive information), so instead we support InformationHiding: agents may expose a function of their state and observations. To achieve security, we utilize ObjectCapabilityModel security patterns. For example, one can use FacetPattern to narrow the interface from one agent to another. ObserverPattern and signal libraries might be considered a naive implementation of this design. They have been used to good effect, but are inflexible and rigid: they don't allow effective support for functions of another actor's state and observations. Done well, we could presumably have an agent represent the state of an entire SQL database, with the argument to the function being an ad-hoc SQL query.

But this leaves unanswered the challenges of affecting the system, and handling concurrency.

If we were only interested in observation and analysis, it would be sufficient to update some local state. Observers could be scheduled to recompute their observations as needed. This corresponds, roughly, to FunctionalReactiveProgramming. But agents need non-local SideEffects, lest you harm their utility as "pluggable" units that will affect a system.

For non-local SideEffects, many systems have resorted to old faithful MessagePassing. Upon observing certain conditions or changes in the environment, the 'agent-actor' hybrid sends some messages to affect other agent-actors in the environment. In addition to observing one another, agents-actors directly receive and send messages. One gets the expressiveness of Actors, and the pluggable nature of agents. Unfortunately, as is the common case with hybrid designs, you also accept the complexities of both: message loss, GarbageCollection issues, order of message arrival, concurrency control. If one isn't very careful, using type and effect systems and such, then a lot of potential optimizations are also hurt. But the combination is promising, and in some ways pays for itself; e.g. it is very easy to create an observable queue and have a bunch of pluggable actor-agents reacting to whether it is full or empty. That is simpler than the queue itself knowing about which actors need to use it, simpler than working with threads.

I pursued a hybrid design, focusing on the ad-hoc observer functions, with a bit of type-system layering to ensure I could still achieve various optimizations. It was, I thought, the best I'd be able to do: distributed actors with access to FunctionalReactiveProgramming-style ad-hoc distributed query functions. I was wrong!

ReactiveDemandProgramming

Suppose instead that agents affect one another through a mechanism just as declarative, reactive, and continuous as the observation itself. In fact, assume observation is a potential source of effect, since that allows some sane behaviors, like demand-driven sensors: one could easily represent an agent that powers up a security camera only while another agent is trying to see the feed. Let's call these 'demand-effects', a limited class of SideEffect that occurs between agents. The resulting paradigm is ReactiveDemandProgramming.

In RDP, all side-effects between agents are demand-effects. Demand-effects are indistinguishable from observer-effects. Observations are reactive and continuous, changing over time, and so are the demand-effects. Demand-effects are idempotent, which allows a huge range of optimizations; for example, ten demands for the same information can be combined into one, with MultiCast, rather than processing the same request ten times. Or if ten different agents share partial structure and state, then they can be partially combined into a single agent with multiple active states. Demand-effects are continuous and concurrent - they are all active at once.

But local effects are still possible.

Based on observations, agents may perform a transition to a new state. During transition, they may spawn new agents or perform other 'discrete' activities. The understanding of events, thus, is entirely local to each agent. The 'new state' allows an agent to keep some memory. Unlike actors, however, RDP doesn't need much non-regenerable memory. Actors programs use a lot of memory for hooking into frameworks, explicit caching, patterns for managing concurrent requests, and for message-queues. RDP agents are hooked in by default, have implicit caching, handle concurrent requests without patterns, and 'agents maintain' communications rather than fire-and-forget, and so all connections are implicit in the actor state and source-code. (This also supports resilience after disruption or persistence.)

Thus, while RDP agents in general are reactive StateMachines, RDP programs in-the-large can get by with very little use of internal state. A bit of short-term memory at the sensors wouldn't hurt, though. And demands can 'drive' real-world state easily enough.

To abstract the construction of agents, one uses an agent that will spawn new agents upon observing the demand. This is a FactoryPattern. The signature I'm considering is Agent -> Agent -> Agent (called Factory -> Spec -> Product). The use of an Agent as a Spec is optional, but does avoid a few semantic issues with a 'continuous, time-varying demand' potentially producing a logically infinite set of Products. Instead, one agent input results in up to one agent output. (No guarantee the result is 'new', and the Product may also be time-varying.)

Implementation isn't anything special. One uses bi-directional subscriptions (use ID to both push the changes to 'demand' and to receive updates). The receiving agent is allowed to use your demands to both control systems and to answer other queries. Thus, supposing we have various agents asking for F(X), F(Y), and F(Z) for some confined and stateless agent F, then the results would be F(X,{X,Y,Z}), F(Y,{X,Y,Z}), and F(Z,{X,Y,Z}). Of course, that is only for confined and stateless agent. A stateful agent could include information from past demands. An unconfined agent could be observing yet another agent G, and be getting results such as: G(X,{X,Y,L,M,N}) and G(Y,{X,Y,L,M,N}).

With the advent of ReactiveDemandProgramming, I think ActorsModel should be retired, along with similar MessagePassing systems - such as ObjectOrientedProgramming. I cannot think of any SoftwareEngineering aspect where ActorsModel or MessagePassing is superior.

Last edit June 1, 2010
