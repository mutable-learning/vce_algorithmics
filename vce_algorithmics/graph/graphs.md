---
jupytext:
  formats: md:myst
  text_representation:
    extension: .md
    format_name: myst
kernelspec:
  display_name: Python 3
  language: python
  name: python3
---
# Graph ADTs

## Description

There is a field of mathematics known as **Graph Theory** where graphs are used to represent the relations between pairs of objects. It just so happens that these graphs have become key tools for helping to develop solutions to many problems found in Computer Science as well. There are many different types of graphs that can be used to model different problems and in this section we will be looking at these graphs, their properties, and their uses in detail.

Objects in a graph are represented by **vertices** and the relationships between objects are displayed with **edges** joining the vertices using a line. There are two main categories of graphs:

```{code-cell} ipython3
:tags: [remove-cell]
from myst_nb import glue
import networkx as nx
import matplotlib.pyplot as plt

G1 = nx.diamond_graph()
fig, ax = plt.subplots(figsize=(6,2))
nx.draw(G1)

G2 = nx.gn_graph(10, seed=1230)
fig2, ax = plt.subplots(figsize=(6,2))
nx.draw(G2)

glue("undirected",fig, display=False)
glue("directed",fig2, display=False)
```

::::{grid}
:gutter: 5

:::{grid-item-card} **Undirected Graphs**
Edges between vertices have no orientation. There are no arrows indicating the *direction* of any edge in the graph. 
+++
```{glue:figure} undirected
:figwidth: 300px
:name: "Undirected Graph"

A simple undirected graph with four vertices and five edges
```
:::

:::{grid-item-card} **Directed Graphs**
Edges between vertices have their orientation set to indicate the *direction* of the edge between vertices.
+++
```{glue:figure} directed
:figwidth: 300px
:name: "Directed Graph"

A directed graph with the arrows showing the orientation of each edge
```
:::

::::

We will go into each of these types of graphs and all their features and differences in much more detail later on. For now though we will state that all graphs can be represented as an abstract data type in the same way you can represent a list or queue.

## Defining Characteristics
Graphs:
- have a set of vertices
- have a set of edges
- vertices and edges can have values associated with them

## Specification

The specification for a Graph ADT will typically contain operations similar to below:

```{prf:definition}
:nonumber:
:class: adt-specification
:label: Graph ADT specification

Name: **Graph**<br/>
Import: $element, boolean, vertex$<br/>
Operations:<br/>
$newGraph: \space \rightarrow graph$<br/>
$addVertex: graph$ x $vertex \rightarrow graph$<br/>
$removeVertex: graph$ x $vertex \rightarrow graph$<br/>
$addEdge: graph$ x $vertex$ x $vertex \rightarrow graph$<br/>
$removeEdge: graph$ x $vertex$ x $vertex \rightarrow graph$<br/>
$setEdgeValue: graph$ x $vertex$ x $vertex$ x $element \rightarrow graph$<br/>
$adjacent: graph$ x $vertex$ x $vertex \rightarrow boolean$<br/>


```