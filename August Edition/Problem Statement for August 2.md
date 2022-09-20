# Problem

Ada has a farm in the shape of a convex polygon. For simplicity, the vertices of the polygon are numbered $1$ through $N$ in clockwise order.

There are many cows living on the farm. Cows fight often, so Ada wants to divide the farm into separate regions using fences to prevent accidents. 
Each fence can be considered a line segment.

Ada is worried about the free space available for each cow, so she needs to know the area of the region inhabited by a particular cow sometimes. 
As her apprentice, your task is to perform $Q$ queries. There are two types of queries:

1. $u$ $v$: Build a fence between vertices $u$ and $v$. It is guaranteed that this fence does not intersect any previously built fence (but they may have common endpoints).
2. $x$ $y$: Find the area of the region inhabited by a cow at position $(x, y)$. 
Sometimes, the point may lie on a fence (the cow is trying to cross the fence); 
it may also be outside the farm or on its border (_the cow is escaping!_). In these cases, the area is $0$.

## Input
- The first line of the input contains a single integer $T$ denoting the number of test cases. 
The description of $T$ test cases follows.
- The first line of each test case contains two space-separated integers $N$ and $Q$.
- $N$ lines follow. For each $i$ ( $1 \le i \le N$ ), the $i$-th of these lines contains two space-separated 
integers $x$ and $y$ denoting the coordinates of the $i$-th vertex.
- Each of the next $Q$ lines contains three space-separated integers describing a query in the above format.

## Output
For each query of the second type, print a single line containing one real number with exactly one decimal place — the area of the given region.

## Constraints
- $1 \le T \le 4$
- $3 \le N \le 10^5$
- $1 \le Q \le 10^5$
- The sum of $N$ over all test cases does not exceed $3 \cdot 10^5$
- The sum of $Q$ over all test cases does not exceed $3 \cdot 10^5$ 
- $1 \le u, v \le N$
- $0 \le x, y \le 2 \cdot 10^9$
- No three vertices are collinear

## Sample 
__Input__

1  
6 5  
5 0  
3 0  
0 3  
2 5  
6 5  
8 3  
2 3 1  
1 4 1  
2 3 1  
1 4 6  
2 6 4  

__Output__

27.0  
11.0  
4.0  

## Explanation

![image](https://user-images.githubusercontent.com/113341054/191193135-cf121e27-a671-4152-822e-312b77a4a80a.png)

The farm is a hexagon as depicted in the picture above. The queries are as follows:

- Query on point $\mathsf{G}$, the answer is the area of the hexagon.
- Add fence $\mathsf{AD}$, the farm is split into two regions.
- Again a query on point $\mathsf{G}$, the answer is the area of region $\mathsf{ABCD}$.
- Add fence $\mathsf{DF}$, the farm is split into three regions in total.
- Query on point $\mathsf{H}$, the answer is the area of region $\mathsf{DEF}$.



