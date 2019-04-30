## Shortest Path in unweighted graph using BFS

Consider the following unweighted graph :

![wpP-uwTqLjyKbnLDbBQJdH8JiyiowNQMZW0j5R_1dL8NB4FeYQ-v1NngHllWY1l7hkRURQx0o1VnpVV8EF1Qz9TWubwFN8HvZFb2O6iv6amzZCDP-N-ad3ClWj7bo2bEwyDW9b77](https://user-images.githubusercontent.com/20956124/56976605-f4522e80-6b90-11e9-9cee-7c0929d66bc4.png)

Suppose we need to find the shortest path from A to all the nodes. That is, We consider the weight of each edge to be 1 and find the shortest path to each node. Let’s run BFS from A.

Along with BFS, we will maintain an array `Dist[ ]` which will store the shortest path from A to each vertex. (For explanation, I will consider indices to be letters).

We initialize Dist `[A] = 0`.

We run BFS. 

Nodes will enter the queue in following order : - 

`A -> B -> C -> D -> E -> F -> G`

Each time a node calls a neighbouring node we increase its distance by 1. 
```
Dist [A] = 0

A->B

Dist [B] = 1

B->C

Dist [C] = 2

C->D

C->E

Dist [D] = 3

Dist [E] = 3

D->F

D->G

Dist [F] = 4

Dist [G] = 4
```

Thus we see we have the shortest distances of all the nodes from A using BFS.
