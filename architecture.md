## Architecture Checklist:

For every new feature:
- Draw the UI
- Decide on the needs of the feature
- Select a proper architectural pattern to use
- Draw the backend classes
- Draw the database
- Write the variables that will be used
- Draw the network connection architecture
- Write the functions, passed variables, returns

### Architectural Patterns:

Our notes on the most common Game Programming Patterns.

#### Common Colonist Patterns:

- Command=>User inputs, rebind keys, replay systems, undo/redo
- Observer=>Achievement, do action after event
- State=>Multiple states, screens, enums, turn, too many if nests, character, object>enum
- Update=>Update objects via graphics, network, sockets
- Subclass Sandbox=>similar objects with different behavior
- Type Object=>Direct class inheritance doesn't work, ex: ostrich, bird but can't fly
- Service Locator=>Like singleton, all services organized together
- Dirty Flag=>Costly operations. Track objects updated

#### Extra Patterns:

- Flyweight=>Large memory using duplicate objects, deep clone
- Prototype=>Clone, spawn, shallow clone
- Singleton=>Only 1 instance, services
- Double Buffer=>display, graphics, dynamic map/grid based on proximity
- Game Loop=>Action games, real time games, animations
- Bytecode=>Modding/game design for non coders
- Component=>Reusable objects. Like Type Object but not coupled
- Event Queue=>Like observer, but queued. For expensive actions with assets
- Data Locality=>Reduces memory used and leaks, reduces lag
- Object Pool=>Deactivates and reuse objects
- Spatial Partition=>Store many objects like map/grid, path finding, collision detection, ray tracing

### Source:
https://gameprogrammingpatterns.com/contents.html  
https://github.com/Habrador/Unity-Programming-Patterns  
https://github.com/Habrador/Unity-Programming-Patterns/tree/master/Assets/Patterns  

### Extra Study Sources:
https://www.youtube.com/watch?v=Eyr7_l5NMds  
https://www.youtube.com/watch?v=wYkzeKghjsI  
https://www.youtube.com/watch?v=eXPBR3WlRGY  
https://www.youtube.com/watch?v=ll6bxQGkyCk  
https://www.youtube.com/watch?v=fGshe3ILKnA  
https://www.youtube.com/watch?v=4qWYjfj5QF8  
https://www.youtube.com/watch?v=MI2vQYP5KYs  
https://www.youtube.com/watch?v=8TIkManpEu4  
https://www.youtube.com/watch?v=Yy7Dt2usGy0  
https://www.youtube.com/watch?v=3O_rpTWdGps  
