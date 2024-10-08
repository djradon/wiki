
- [[p.attributedTo]] @alex-martelli

## Resources

- https://devopedia.org/duck-typing
  - [[p.hasHighlight]]
    - With [[t.cs.goose-typing]], the interface or protocol is made explicit. This is done using an Abstract Base Class (ABC). In the call isinstance(obj, cls), the second argument must be an ABC. The ABC class itself can't be instantiated but another class provides an implementation of the expected interfaces. However, this other class is simply registered (via a decorator) as conforming to the ABC's interface; that is, it's not explicitly derived from the ABC. For this reason, we call goose typing as "virtual subclassing of Python ABCs." 