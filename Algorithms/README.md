# Algorithms

## Algorithm Analysis
* [Khan Academy - Asymptotic Notation](https://www.khanacademy.org/computing/computer-science/algorithms/asymptotic-notation/a/asymptotic-notation)
* [Wikipedia - Analysis of Algorithms](https://en.wikipedia.org/wiki/Analysis_of_algorithms)
* [A Gentle Introduction to Algorithm Complexity](http://discrete.gr/complexity/)
* [Princeton - An Introdution to the Analysis of Algorithms](http://aofa.cs.princeton.edu/home/)
* [Big-O Cheat Sheet](https://drive.google.com/folderview?id=0B9l0_ldK09SOfjE3R1c2LTcxSU8xSGxXNkJpOF9iQ0JMV1NLUDhnUmlXVm50R0tLTGFUeEE)

## Amortized Analysis
* [Wikipedia - Amortized Analysis](https://en.wikipedia.org/wiki/Amortized_analysis)
* [Stack Overflow - Amortized Analysis](http://stackoverflow.com/questions/11102585/what-is-amortized-analysis-of-algorithms)

## Textbooks
* Cormen, Leiserson, Rivest, and Stein - Introduction to Algorithms
* Skiena - The Algorithm Design Manual

## Courses
* [Standford + Coursera - Algorithms: Design and Analysis, Part 1](https://www.coursera.org/course/algo)
* [Princeton + Coursera - Algorithms, Part I](https://www.coursera.org/course/algs4partI)
* [Udacity - Intro to Algorithms: Social Network Analysis](https://www.udacity.com/course/intro-to-algorithms--cs215)

## Sorting
![sorting algorithm comparison](https://d262ilb51hltx0.cloudfront.net/max/800/1*w3vKy_JFKd50dixxFkpPPg.png)

### Selection Sort
* Repeatedly extracts the smallest remaining element from the unsorted part of the set.
* ![selection sort psuedocode](https://lh3.googleusercontent.com/9U_qAi6-IepChS14HEFKXYbpxc3ydStU96qK3VkA3i9BzO8KxXqSNFXgxgJNyFHR9h-QvAx9aVRxCtJGaA-4DtUoZtqvA4GpLf6-1fWAhHljIKgagnhDoR3-Sc65LZhoal3y3mut5qFA-lY-XZDn85BuLLC0xi_35ao_JBhkHpp0iAmY9kJxzJXMVMei84c7P9Y9qtEprTmRtherRo0W9BmOyHIT4kryv4hrzxcPBcOzWsovbHwn4aJMGEn9cVJ1984IB31-Z4vDBGjQPig79DeFXl8FZDEzbx7y1Z4Y9KBSfivdQG1NneKn5pYS64tFyUsZWj9kzD2YECMlfMVImniNBFn0xHb452FPD4IQKtPeiv2E4Xzzc4HSTvypFmuEjExkmt7oewESAxeYQPVp5XqIUgrsGvamSm8msUsPugi7MBnh72VgWPQhKHboFej7mzXNHiuiZyeOPO1YndQGroyjKqt3GhHUpgCDtqfHltKRUe1UGlagIN2HAwXy0iCmP0bIRu5TRJHthF55x5hynCa4UZUh5iMYRYkthDR8U_xmpvICSlJP4BQ2LZrXEGDuz48kpYYJzdC0kCFF0nyR2-qpJMGUE38=w248-h90-no)
* ![selection sort animation](https://upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Selection_sort_animation.gif/250px-Selection_sort_animation.gif)
* Poor performance, but easy to remember.

| Worst Case       | Average Case     | Best Case        | Worst Case (Space)         |
|------------------|------------------|------------------|----------------------------|
| O(n<sup>2</sup>) | O(n<sup>2</sup>) | O(n<sup>2</sup>) | O(n) total, O(1) auxillary |

### Mergesort
  * Requires more memory than Quicksort, but is faster in the worst case
  * ![merge sort psuedocode](http://www2.hawaii.edu/~suthers/courses/ics311s16/Notes/Topic-02/code-merge-sort.jpg)
  * ![merge sort animation](https://upload.wikimedia.org/wikipedia/commons/c/cc/Merge-sort-example-300px.gif)

| Worst Case | Average Case | Best Case                               | Worse Case (Space) |
|------------|--------------|-----------------------------------------|--------------------|
| O(n log n) | O(n log n)   | O(n log n) typical,O(n) natural variant | O(n)               |

### Quicksort
 * [Wikipedia Article on Quicksort](https://en.wikipedia.org/wiki/Quicksort)
 * "Typically, quicksort is significantly faster in practice than other Θ(nlogn) algorithms, because its inner loop can be efficiently implemented on most architectures, and in most real-world data, it is possible to make design choices which minimize the probability of requiring quadratic time."
 * Low memory requirement

| Worst Case       | Average Case | Best Case          | Worse Case (Space)       |
|------------------|--------------|--------------------|--------------------------|
| O(n<sup>2</sup>) | O(n log n)   | O(n log n) or O(n) | O(n) (naive) or O(log n) |

### Heapsort
* [Heapsort Visualization](https://www.cs.usfca.edu/~galles/visualization/HeapSort.html)
* Build a heap from the data, then repeatedly extract the min/max

| Worst Case       | Average Case | Best Case          | Worse Case (Space)       |
|------------------|--------------|--------------------|--------------------------|
| O(n log n)       | O(n log n)   | Ω(n), O(n log n)   | O(1)                     |

### BST Sort
* TODO

## Searching / Graph Traversal

### Binary Search
* TODO

### Breadth-First
* TODO

### Depth-First
* TODO

### Uniform-Cost/Dijkstra's
* TODO

### A*
* TODO

### NP-Complete Problems
* [Wikipedia - NP-Completeness](https://en.wikipedia.org/wiki/NP-completeness)
* "In computational complexity theory, a decision problem is NP-complete when it is both in NP and NP-hard. The set of NP-complete problems is often denoted by NP-C or NPC. The abbreviation NP refers to "nondeterministic polynomial time". Although any given solution to an NP-complete problem can be verified quickly (in polynomial time), there is no known efficient way to locate a solution in the first place; indeed, the most notable characteristic of NP-complete problems is that no fast solution to them is known."

## Travelling Salesman Problem (TSP)
* Travelling Salesman Problem | Set 1 (Naive and Dynamic Programming)
Travelling Salesman Problem (TSP): Given a set of cities and distance between every pair of cities, the problem is to find the shortest possible route that visits every city exactly once and returns to the starting point.
Note the difference between Hamiltonian Cycle and TSP. The Hamiltoninan cycle problem is to find if there exist a tour that visits every city exactly once. Here we know that Hamiltonian Tour exists (because the graph is complete) and in fact many such tours exist, the problem is to find a minimum weight Hamiltonian Cycle.

* ![Traveling Salesmans City Image](http://d1gjlxt8vb0knt.cloudfront.net//wp-content/uploads/Euler12.png)


For example, consider the graph shown in figure on right side. A TSP tour in the graph is 1-2-4-3-1. The cost of the tour is 10+25+30+15 which is 80.

The problem is a famous NP hard problem. There is no polynomial time know solution for this problem.

Following are different solutions for the traveling salesman problem.

*Naive Solution:
1) Consider city 1 as the starting and ending point.
2) Generate all (n-1)! Permutations of cities.
3) Calculate cost of every permutation and keep track of minimum cost permutation.
4) Return the permutation with minimum cost.

Time Complexity: ?(n!)

####Dynamic Programming:
Let the given set of vertices be {1, 2, 3, 4,….n}. Let us consider 1 as starting and ending point of output. For every other vertex i (other than 1), we find the minimum cost path with 1 as the starting point, i as the ending point and all vertices appearing exactly once. Let the cost of this path be cost(i), the cost of corresponding Cycle would be cost(i) + dist(i, 1) where dist(i, 1) is the distance from i to 1. Finally, we return the minimum of all [cost(i) + dist(i, 1)] values. This looks simple so far. Now the question is how to get cost(i)?
To calculate cost(i) using Dynamic Programming, we need to have some recursive relation in terms of sub-problems. Let us define a term C(S, i) be the cost of the minimum cost path visiting each vertex in set S exactly once, starting at 1 and ending at i.
We start with all subsets of size 2 and calculate C(S, i) for all subsets where S is the subset, then we calculate C(S, i) for all subsets S of size 3 and so on. Note that 1 must be present in every subset.

####If size of S is 2, then S must be {1, i},
    C(S, i) = dist(1, i) 
    Else if size of S is greater than 2.
     C(S, i) = min { C(S-{i}, j) + dis(j, i)} where j belongs to S, j != i and j != 1.
For a set of size n, we consider n-2 subsets each of size n-1 such that all subsets don’t have nth in them.
Using the above recurrence relation, we can write dynamic programming based solution. There are at most O(n*2n) subproblems, and each one takes linear time to solve. The total running time is therefore O(n2*2n). The time complexity is much less than O(n!), but still exponential. Space required is also exponential. So this approach is also infeasible even for slightly higher number of vertices. Answer provided by geekforgeeks



## Knapsack
* 
Given weights and values of n items, put these items in a knapsack of capacity W to get the maximum total value in the knapsack. In other words, given two integer arrays val[0..n-1] and wt[0..n-1] which represent values and weights associated with n items respectively. Also given an integer W which represents knapsack capacity, find out the maximum value subset of val[] such that sum of the weights of this subset is smaller than or equal to W. You cannot break an item, either pick the complete item, or don’t pick it (0-1 property).

A simple solution is to consider all subsets of items and calculate the total weight and value of all subsets. Consider the only subsets whose total weight is smaller than W. From all such subsets, pick the maximum value subset.

1) Optimal Substructure:
To consider all subsets of items, there can be two cases for every item: (1) the item is included in the optimal subset, (2) not included in the optimal set.
Therefore, the maximum value that can be obtained from n items is max of following two values.
1) Maximum value obtained by n-1 items and W weight (excluding nth item).
2) Value of nth item plus maximum value obtained by n-1 items and W minus weight of the nth item (including nth item).

If weight of nth item is greater than W, then the nth item cannot be included and case 1 is the only possibility.

2) Overlapping Subproblems
Following is recursive implementation that simply follows the recursive structure mentioned above.

####
    /* A Naive recursive implementation of 0-1 Knapsack problem */
    #include<stdio.h>
 
    // A utility function that returns maximum of two integers
    int max(int a, int b) { return (a > b)? a : b; }
 
    // Returns the maximum value that can be put in a knapsack of capacity W
    int knapSack(int W, int wt[], int val[], int n)
    {
       // Base Case
       if (n == 0 || W == 0)
           return 0;
 
       // If weight of the nth item is more than Knapsack capacity W, then
       // this item cannot be included in the optimal solution
       if (wt[n-1] > W)
           return knapSack(W, wt, val, n-1);
 
       // Return the maximum of two cases: 
       // (1) nth item included 
       // (2) not included
       else return max( val[n-1] + knapSack(W-wt[n-1], wt, val, n-1),
                        knapSack(W, wt, val, n-1)
                      );
    }
 
    // Driver program to test above function
    int main()
    {
        int val[] = {60, 100, 120};
        int wt[] = {10, 20, 30};
        int  W = 50;
        int n = sizeof(val)/sizeof(val[0]);
        printf("%d", knapSack(W, wt, val, n));
        return 0;
    }
####
      // Driver program to test above function
    int main()
    {
        int val[] = {60, 100, 120};
        int wt[] = {10, 20, 30};
        int  W = 50;
        int n = sizeof(val)/sizeof(val[0]);
        printf("%d", knapSack(W, wt, val, n));
        return 0;
    }
        Output: 220
It should be noted that the above function computes the same subproblems again and again. See the following recursion tree, K(1, 1) is being evaluated twice. Time complexity of this naive recursive solution is exponential (2^n).

Since suproblems are evaluated again, this problem has Overlapping Subprolems property. So the 0-1 Knapsack problem has both properties (see this and this) of a dynamic programming problem. Like other typical Dynamic Programming(DP) problems, recomputations of same subproblems can be avoided by constructing a temporary array K[][] in bottom up manner. Following is Dynamic Programming based implementation.

####
    // A Dynamic Programming based solution for 0-1 Knapsack problem
    #include<stdio.h>
 
    // A utility function that returns maximum of two integers
    int max(int a, int b) { return (a > b)? a : b; }
 
    // Returns the maximum value that can be put in a knapsack of capacity W
    int knapSack(int W, int wt[], int val[], int n)
     {
       int i, w;
       int K[n+1][W+1];
 
       // Build table K[][] in bottom up manner
      for (i = 0; i <= n; i++)
       {
          for (w = 0; w <= W; w++)
           {
               if (i==0 || w==0)
                   K[i][w] = 0;
              else if (wt[i-1] <= w)
                   K[i][w] = max(val[i-1] + K[i-1][w-wt[i-1]],  K[i-1][w]);
               else
                     K[i][w] = K[i-1][w];
         }
       }
 
       return K[n][W];
       }
 
       int main()
       {
        int val[] = {60, 100, 120};
        int wt[] = {10, 20, 30};
        int  W = 50;
        int n = sizeof(val)/sizeof(val[0]);
        printf("%d", knapSack(W, wt, val, n));
        return 0;
        }
Solution by geekforgeeks        
