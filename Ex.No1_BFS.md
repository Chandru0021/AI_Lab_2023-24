# Ex.No: 1  Implementation of Breadth First Search 
### DATE:17_02_2024                                                                            
### REGISTER NUMBER : 212221060144
### AIM: 
To write a python program to implement Breadth first Search. 
### Algorithm:
1. Start the program
2. Create the graph by using adjacency list representation
3. Define a function bfs and take the set “visited” is empty and “queue” is empty
4. Search start with initial node and add the node to visited and queue.
5. For each neighbor node, check node is not in visited then add node to visited and queue list.
6.  Creating loop to print the visited node.
7.   Call the bfs function by passing arguments visited, graph and starting node.
8.   Stop the program.
### Program:
```
def dfs(graph, node, visited):
    if node not in visited:
        print(node, end=' ')
        visited.add(node)
        if node in graph:
            for neighbor in graph[node]:
                dfs(graph, neighbor, visited)

# Given partial graph
graph = {
    '1': ['2', '3'],
    '2': ['4', '5'],
    '3': ['6', '7'],
}

# Set to keep track of visited nodes
visited = set()

# Perform DFS traversal starting from each node if not visited
print("DFS traversal starting from each node:")
for node in graph:
    dfs(graph, node, visited)
```

### Output:
DFS traversal starting from each node:
1 2 4 5 3 6 7 

### Result:
Thus the breadth first search order was found sucessfully.
