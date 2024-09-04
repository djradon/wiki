
- [[c.software.database.graph.property]]
- [[p.isComponentOf]] [[prdct.sigma-js]]
- [[c.resource]]
  - https://archive.fosdem.org/2017/schedule/event/graph_library_javascript/attachments/slides/1803/export/events/attachments/graph_library_javascript/slides/1803/Graphology___FOSDEM_2017.pdf


## Examples

### native filtering

```
// From a filtering function
const sub = subgraph(graph, function (key, attr) {
  return key.startsWith('J') || attr.color === 'red';
});
```

### copying to array (from @chatgpt.3.5), yuck

```
const { Graph } = require('graphology');

const graph = new Graph();

graph.addNode('Alice', { age: 30 });
graph.addNode('Bob', { age: 25 });

const nodesOver25 = Array.from(graph.nodes()).filter(node => graph.getNodeAttribute(node, 'age') > 25);
```