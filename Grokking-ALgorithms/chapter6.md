## Graph
- example find the smallest route for a path.
- You’re always trying to find the shortest something. It could
be the shortest route to your friend’s house. It could be the smallest
number of moves to checkmate in a game of chess. The algorithm to
solve a shortest-path problem is called breadth-first search.


To figure out how to get from Twin Peaks to the Golden Gate Bridge,
there are two steps:
1. Model the problem as a graph.
2. Solve the problem using breadth-first search.


### What's a Graph?
- Graph is a node and edge to connect things between each other.
a node could have many edges to be connected to multiple nodes. Nodes connected to each other are called neighbours.


### Breadth-first search:
It helpd answer two types of questions:
• Question 1: Is there a path from node A to node B?
• Question 2: What is the shortest path from node A to node B?


--> In Breadth first you need to search things in the order they added. That's why we use Queues `` first in.. first out``
```
Queues are similar to stacks. You can’t
access random elements in the queue.
Instead, there are two only operations,
enqueue and dequeue.

```

- Enqueue: add item to the end of the queue.
- Dequeue: remove first item from queue


## Implementing Graph:

- You can implement graph using hash table a node could be a key and its neighnours will be array of values.
```
 let graph = {};
 graph['street1'] = ['street2','street3','street4']
```
### Types of Graph:

- a directed graph, the relationship is only one way.
- An undirected graph doesn’t have any arrows, and both nodes are each other’s neighbors.


## Breadth First:
- queue = [...graph[element]]; --> node with its neighbours
- searched =[]
- while(queue) ``Queue has elements``
    neighbour=queue.dequeue();
    if neigbour not in searched
    if element ``Match Condition ``
    return element 
    else
     queue = [...queue, graph[neighbour]]
     searched.append(neighbour)

### Running time
- If you search your entire network for a mango seller, that means you’ll
follow each edge. So the running time is at least O(number of
edges).
You also keep a queue of every person to search. Adding one person to
the queue takes constant time: O(1). Doing this for every person will
take O(number of people) total. Breadth-first search takes O(number of
people + number of edges), and it’s more commonly written as O(V+E)
(V for number of vertices, E for number of edges).

-----------------------------

**NB**: A tree is a special type of graph, where no edges
ever point back