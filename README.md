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

#Rules for determining the algorithm running time:
1. Running time of statements inside the loop multiplied by the no. of iterations,

    Running time = no. of iterations * statement(s) runtime  
        nc = n * c  
      O(n) = n * c (Big O notation format) and c is execution time for statements
      
2. Nested Loops:  
    Running time = product of size of all loops  
        nc = n * n * c - (n are representing the two loops)  
        nc = n<sup>2</sup> * c  
        O(n<sup>2</sup>) = n * c (Big O notation format) and c is execution time for statements
    
3. Consecutive statements  
    Running time = product of size of all loops + Add the complexity of each statement
        nc = c0 + c1n + c2n<sup>2</sup>  
        O(n<sup>2</sup>) = c0 + c1n + c2n<sup>2</sup>
        
        For e.g. :Consider below consecutive loop
        i  = i+2; // constant time c0
        for(int j=0; j<=n; j++ {
            // statement 1 (c1)
            for(int k=0; k<=n; k++ {
                for(int l=0; l<=n; l++ {
                    //statement c2
                }
            }
        }
4. If then else statements  
    Running time = test time + (then or else part)  
    // Remember if or then whichever has higher value is chosen  
    ```
    if(i == 2) {
        return false; // constant c1
    }
    else  {
        for(int k=0; k<=n; k++ {
            k = k +1; // constant c2
        }
    }
    ```
   Total time  = c0 + c2(n)  
   O(n) = c0 + c2(n)
   
5. Logarithmic complexity:  
    If the algorithm takes a constant time to divide the problem size by fraction then it's represented by O(log n)  
    
    ```
    for(int i=0; i<=n; i++) {
        i = i*2; // O(log n)
    }
   ```
   at k<sup>th</sup> step, 2<sup>k</sup> = n  
   taking log on both sides  
   log(2<sup>k</sup>) = log n  
   k log 2 = log n  
   O( log n) = k  
   
# Asymptotic notation  
    1. Big O notation
        - Upper bounding function
            - f(n) = O(g(n)) where f(n) represents the large value of n
             - O(g(n)) = f(n) for positive constants 'c' and 'n0' this means
                    0<= f(n) <= cg(n) for all n >= n0
            - g provides the upper bound (Upper bound = max time it takes to execute) and c is a constant which depends on
                - Programming language,
                - CPU Speed
                - Memory size,
                - Algorithm
            - Always remember to write the Upper bound as Closest one
            
    2. Omega notation
        - Lower bound function
        - Means function will be executed in this min time  
            - f(n) = Omega (g(n)) // n has larger values and g(n) reprresents the lower bound of f(n)
            - 2\n<sup>2</sup> + n >= c2.g(n)
    3. Theta notation
        - It is also called as Order function
        - decides if the upper and lower bouds are same
            - n(g(n)) = Positive constants c1, c2 and n0 such that
            O<=  c1g(n) <= f(n) <= c2g(n) for all n<= n0
            
        