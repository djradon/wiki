
- https://www.w3.org/DesignIssues/Diff

## Summary

- discusses what patches could look like, but no concrete solutions?

## Highlights

### Weak and Strong diffs

To address robustness, we distinguish two types of RDF graph deltas: a _weak_ delta gives enough information to apply it to exactly the graph it was computed from, but a _strong_ delta specifies the changes in a context-independent manner. The difference is not in the patch file format, but in the information a particular patch gives.

