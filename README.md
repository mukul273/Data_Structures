## This is a practise for 
# Data Structures using Java 8

Some Concepts  
###Recursion: 
A recursive function is one which calls itself. During each recursive call a given problem is broken into smaller problem.

##Base case recursion:  
This means that the case where the function doesn't recur anymore.
This also means this is where recursion terminates.

##Recursive case:
This is the case where functions calls itself to perform subtask.

It is important to understand that we have to reduce teh size of the
problem in recursive case so that we can reach the base case quickly.

Generally iterative solutions are more efficient than recursive solutions
For e.g.: Factorial, Fibonacci, Merge Sort, Quick Sort, Binary search, Tree/Graph traversal,
Tower of hanoi etc.

Comparison between Recursion and Iteration

    Recursion                              | Iteration
    ---------------------------------------|-----------------------------
    1. Termination when base case reached  | 1. Termination when condition is false
    2. Requires extra space for each       | 2. Not Requried
    recursive call                          
    3. Stack overflow can occur if infinite| 3. Infinite loop can run forever
    recursion,

###Back tracking
Searches for solution to a problem among the all available solutions  
It is also sort of Brute force,
This is if the problem is not solved then go back to the recursion that has other solution,
The optimization can be done by not going all the way back to the start.  
e.g: Generating all binary strings, N-Queen problem, Knapsack problem, Graph coloring etc.

