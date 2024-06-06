# Graph Implementation in JavaScript

This repository contains a simple implementation of a graph data structure using JavaScript classes. The graph supports adding and removing vertices, edges, and performing depth-first search (DFS) and breadth-first search (BFS) traversals.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
  - [Creating a Graph](#creating-a-graph)
  - [Adding Vertices and Edges](#adding-vertices-and-edges)
  - [Removing Vertices and Edges](#removing-vertices-and-edges)
  - [Performing DFS and BFS](#performing-dfs-and-bfs)
- [License](#license)

## Installation

To use this code, simply copy the `graph.js` file into your project directory.

## Usage

### Creating a Graph

To create a new graph, import the `Graph` and `Node` classes from the `graph.js` file:

```javascript
const { Graph, Node } = require("./graph");
```

Then, create a new instance of the `Graph` class:

```javascript
const graph = new Graph();
```

### Adding Vertices and Edges

To add vertices to the graph, create new instances of the `Node` class and use the `addVertex` method:

```javascript
const node1 = new Node(1);
const node2 = new Node(2);

graph.addVertex(node1);
graph.addVertex(node2);
```

To add edges between vertices, use the `addEdge` method:

```javascript
graph.addEdge(node1, node2);
```

### Removing Vertices and Edges

To remove vertices from the graph, use the `removeVertex` method:

```javascript
graph.removeVertex(node1);
```

To remove edges between vertices, use the `removeEdge` method:

```javascript
graph.removeEdge(node1, node2);
```

### Performing DFS and BFS

To perform a depth-first search (DFS) starting from a specific vertex, use the `depthFirstSearch` method:

```javascript
const dfsResult = graph.depthFirstSearch(node1);
console.log(dfsResult); // Output: [Node { value: 1, adjacent: Set { Node { value: 2, adjacent: Set { Node { value: 1, adjacent: [Set] } } } } }]
```

To perform a breadth-first search (BFS) starting from a specific vertex, use the `breadthFirstSearch` method:

```javascript
const bfsResult = graph.breadthFirstSearch(node1);
console.log(bfsResult); // Output: [Node { value: 1, adjacent: Set { Node { value: 2, adjacent: Set { Node { value: 1, adjacent: [Set] } } } } }]
```

## License

This code is licensed under the MIT License. See the `LICENSE` file for more information.
