
- aka: tagged union or algebraic data type

## Examples

### Weave

```typescript
export type Inclusion =
  | {
    type: "git";
    name?: string;
    url: string;
    options?: GitOptions;
    order?: number;
  }
  | {
    type: "web";
    name?: string;
    url: string;
    options?: HttpOptions;
    order?: number;
  }
  | {
    type: "local";
    name?: string;
    url: string;
    options?: LocalOptions;
    order?: number;
  };
```
