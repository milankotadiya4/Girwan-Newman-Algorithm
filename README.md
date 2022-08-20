# Girwan-Newman-Algorithm
Girvan-Newman method is one of the classic community clustering techniques. By using the algorithm, we are able to separate the network into communities, and the community detection can be used as a good start of data preprocessing.

# **Girvan-Newman Iteration:**

First we need to compute the edge betweenness of every edge in the graph

1. Select a node X, and perform BFS to find number of shortest path from the node X to each node, and assign the numbers as score to each node.
2. Starting from the leaf nodes, we calculate the credit of edge by (1 + (sum of the edge credits to the node) )*(score of destination node / score of starting node)
3. Compute the edge credits of all edges in the graph G, and repeat from step 1. until all of the nodes are selected
4. Sum up all of the edge credit we compute in step 2 and divide by 2, and the result is the edge betweenness of edges.

Next, we remove the edges with the highest edge betweenness, and repeat until we find the good community split.

5. Remove the edges with the highest edge betweenness

6. Compute the modularity Q of the communities split

7. Repeat from step 1, if Q is greater than 0.3–0.7.
