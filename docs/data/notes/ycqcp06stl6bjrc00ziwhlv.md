
- repo: https://gitea.moonside.games/MoonsideGames/MoonTools.ECS

## Features

- "MoonTools.ECS implements all the important parts of ECS, with two additions. the common one is entity relations, which we will talk about later in the tutorial. lots of ECS libraries include relations, which are basically components that are associated with two entities instead of just one.

the uncommon feature which i think makes MoonTools.ECS extremely special is messages. i explain this later in the tutorial as well, but messages are stores of data like components that can be sent by systems and read by other systems. messages are destroyed at the end of every frame. this allows systems to easily communicate in a loosely coupled way, i.e. without directly referencing each other. messages solve a huge number of problems that come up with the ECS architecture, and substantially reduce overall awkwardness."
  - https://blood.church/posts/2023-09-25-shmup-tutorial

## Limitations

- "you can't iterate over all the components attached to an entity in MoonTools.ECS (at least not in release mode) because it has performance implications: creating the iterators means boxing the components. you can however iterate over all the relationships a component has. so we instead need to model traits as entities and "having a trait" is a kind of relation between the character entity and the trait entity."


## Resources

- [[course.shmup-tutorial]] https://cohost.org/prophetgoddess/post/2964176-i-made-a-tutorial-on
- https://cohost.org/prophetgoddess/post/845893-declarative-crusader
  - mentions [[game.pentiment]]