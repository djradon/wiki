
- if you're updating dataset pointers to the current version, you're mutating the source but the principle of immutability is preserved in that the old data still exists and is discoverable from the catalog
- sometimes, e.g., for compliance reasons, you have to hard delete a resource (as opposed to just tombstoning it, a soft delete)

## References

https://s11.no/2013/prov/resources-that-change-state/