
## Summary

- For Flow of Control Dependencies, inject dependencies as interfaces, or abstractions.
- Ensure the abstractions, or interfaces, are defined in a higher level module and implemented in a lower level module to ensure the Source Code Dependency is Inverted.

## Details

- Flow of Control Dependency — when you are debugging code and the line of execution goes from one project into another project or dll.
- Source Code Dependency — where one project references another project or dll.
- We invert a Source Code Dependency when we identify that the rate of change of a project is more than the project that depends on it.
- an Abstraction is an interface and a Detail is an implementation.

## [[c.conclusion]]

- For Flow of Control Dependencies, inject dependencies as interfaces, or abstractions.
- Ensure the abstractions, or interfaces, are defined in a higher level module and implemented in a lower level module to ensure the Source Code Dependency is Inverted.

## Resources

- 1: https://medium.com/codex/the-difference-between-dependency-inversion-and-dependency-injection-15935337ca1b
