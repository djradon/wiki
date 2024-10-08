
- [[c.software.entity-component-system]] [[t.cs.entity-component-system]]
- repo: https://github.com/NateTheGreatt/bitECS
- written-in: javascript
- [[p.usedBy]] [[prdct.ethereal-engine]] [[prdct.hubs]] [[prdct.matrix]] [[prdct.third-room]]
- [[p.hasClientSupport]]
  - [[prdct.element]] [[prdct.babylon-js]]
  - [[prdct.phaser]]

## [[p.hasFeature]]

🔮 Simple, declarative API 	
🔥 Blazing fast iteration
🔍 Powerful & performant queries 
💾 Serialization included
🍃 Zero dependencies 	
🌐 Node or browser
🤏 ~5kb minzipped 	
🏷 TypeScript support
❤ Made with love 	
🔺 glMatrix support

## Interesting

- "bitECS has no built-in concept of systems. We frequently refer the functions invoked during the game loop as “systems”, but there is no formal construct."

## [[c.faq]]

- Is there a string type for components?
  - Strings are expensive and usually unnecessary to have the ECS handle. Instead, create a mapping of integers to strings, and store the integers in the component data as a reference to a string. This makes string serialization minimal and  

## Resources

### Learning Resource

- https://github.com/ourcade/phaser3-bitecs-getting-started
- https://www.youtube.com/playlist?list=PLNwtXgWIx3rhz72-UxKLdCDdqFsnwNc_u

