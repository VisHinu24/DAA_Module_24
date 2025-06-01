# EX 6C TRAVELLING SALES MAN PROBLEM
## DATE: 25-05-25
## AIM:
To Solve Travelling Sales man Problem for the following graph.

![image](https://github.com/user-attachments/assets/653921a4-3d7b-4691-9b41-735e80f7af0b)



## Algorithm :

1.Take the cost matrix that shows the cost between every pair of cities.

2.Generate all possible orders (permutations) in which the cities can be visited.

3.For each order, calculate the total travel cost, including returning to the starting city.

4.Keep track of the minimum total cost found so far.

5.After checking all possible orders, return the minimum cost as the final answer.

## Program :
```
/*
 Developed by: Vishinu H
 Register Number:  212223220124
*/
from sys import maxsize
from itertools import permutations
V = 4
 

def travellingSalesmanProblem(graph, s):
 
    #Write your code
    vertex = [i for i in range(V) if i  != s]
    min_path = maxsize
    next_perm = permutations(vertex)
    
    for p in next_perm:
        curr = 0
        k = s
        
        for i in p:
            curr += graph[k][i]
            k = i
        curr += graph[k][s]
        min_path = min(min_path, curr)
        
    return min_path
 
 

if __name__ == "__main__":
 
    graph = [[0, 10, 15, 20], [10, 0, 35, 25], [15, 35, 0, 30], [20, 25, 30, 0]]
    s = 0
    print(travellingSalesmanProblem(graph, s))
```

## Output :

![image](https://github.com/user-attachments/assets/ecf9c7a0-3e7b-445b-96cd-5a069c62bebc)


## Result :

Thus the program was executed successfully for finding the minimum cost to vist all cities.
