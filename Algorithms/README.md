# Algorithms
[Dictionary of Algorithms and Data Structures](https://xlinux.nist.gov/dads/)

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

You may find this visualizer helpful in understanding some of these algorithms: [http://jasonpark.me/AlgorithmVisualizer/](http://jasonpark.me/AlgorithmVisualizer/). It is worth noting that the visualization of N-queens uses a brute-force algorithm, whereas there are faster known algorithms as discussed below.

## Sorting
![sorting algorithm comparison](https://d262ilb51hltx0.cloudfront.net/max/800/1*w3vKy_JFKd50dixxFkpPPg.png)

### Selection Sort
* Repeatedly extracts the smallest remaining element from the unsorted part of the set.
* ![selection sort psuedocode](http://i.imgur.com/v4nmfxF.png)
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
* Performs an [in-order traversal](http://visualgo.net/bst) over a Binary Search Tree

| Worst Case            | Average Case | Best Case  | Worst Case (Space) |
|-----------------------|--------------|------------|--------------------|
| O(n log n) (balanced) | O(n log n)   | O(n log n) | Θ(n)               |

## Searching / Graph Traversal

### Binary Search
* Binary search, or logarithmic search, is a search algorithm that finds the position of a target value within a sorted array. Simply put, divide and conquer. It works by comparing the target value to the middle element of the array and if they are unequal, the lower or upper half of the array is eliminated depending on the result and the search is repeated in the remaining subarray until it is successful. 

| Worst Case            | Average Case | Best Case  |       Worst Case (Space)        |
|-----------------------|--------------|------------|---------------------------------|
|       O(log n)        |     O(log n) |    O(1)    | O(1) iterative O(log n) recursive

### Breadth-First
* Breadth-first search is an algorithm for traversing tree or graph data structures. It starts at the tree root or node, searching nearby elements first before moving the next level elements. 
 
| Worst Case            |                                 Worst Case (Space)        |
|-----------------------|-----------------------------------------------------------|
|       O(V)=O(b<sup>d) |           O(E)=O (b<sup>d)


### Depth-First
* Like the Breadth-first, DF traverses trees and graphs, except it travels as far as possible on a branch before exploring.
  b is branching factor, d is depth of search.

| Worst Case (Without Repetition)| (Implicit) |  Worst Case (Space)                |
|--------------------------------|------------|------------------------------------|
|       O(E)                     | O(b<sup>d) | O(V)

### Uniform-Cost/Dijkstra's
* Search algorithm for graphs which has many variants, known as Uniform-Cost or Best-search first (A.I.) The original finds the shortest path between two nodes and the first variant finds the shortest path given a static node and uses a min-priority queue.

| Worst Case  
|---------------------------|
| O(E + V  logV)   

### A*
* Search algorithm for graphs and pathfinding known for its performance and accuracy in plotting a path through multiple nodes. 
 It is widely used, for example in gaming, although it can be outperformed by algorithms which pre-load the graph.

| Worst Case            | Worst Case (Space)                                        |
|-----------------------|-----------------------------------------------------------|
| O(E)=O(b<sup>d)       | O(V)=O (b<sup>d)

### NP-Complete Problems
* [Wikipedia - NP-Completeness](https://en.wikipedia.org/wiki/NP-completeness)
* "In computational complexity theory, a decision problem is NP-complete when it is both in NP and NP-hard. The set of NP-complete problems is often denoted by NP-C or NPC. The abbreviation NP refers to "nondeterministic polynomial time". Although any given solution to an NP-complete problem can be verified quickly (in polynomial time), there is no known efficient way to locate a solution in the first place; indeed, the most notable characteristic of NP-complete problems is that no fast solution to them is known."

## Travelling Salesman Problem (TSP)
* Travelling Salesman Problem (TSP): Given a set of cities and distance between every pair of cities, the problem is to find the shortest possible route that visits every city exactly once and returns to the starting point.
Note the difference between Hamiltonian Cycle and TSP. The Hamiltoninan cycle problem is to find if there exist a tour that visits every city exactly once. Here we know that Hamiltonian Tour exists (because the graph is complete) and in fact many such tours exist, the problem is to find a minimum weight Hamiltonian Cycle.

![TSP](http://d1gjlxt8vb0knt.cloudfront.net//wp-content/uploads/Euler12.png)

* The problem is a famous NP hard problem. There is no polynomial time solution for this problem. Naive solution uses a recursive step, and there is a dynamic solution, although both are infeasible.  Approximate algorithm using MST is best alternative. 

## Knapsack
* The knapsack problem or rucksack problem is a problem in combinatorial optimization: Given a set of items, each with a weight and a value, determine the number of each item to include in a collection so that the total weight is less than or equal to a given limit and the total value is as large as possible. It derives its name from the problem faced by someone who is constrained by a fixed-size knapsack and must fill it with the most valuable items. [Knapsack] (https://en.wikipedia.org/wiki/Knapsack_problem#Solving)

## Dynamic Programming
* [Wikipedia - Dynamic Programming](https://en.wikipedia.org/wiki/Dynamic_programming#Dynamic_programming_in_computer_programming)
* [Hackerrank - Dynamic Programming Basics](https://www.hackerrank.com/challenges/maxsubarray/topics/dynamic-programming-basics)
* [MIT OCW - Dynamic Programming I](http://ocw.mit.edu/courses/electrical-engineering-and-computer-science/6-006-introduction-to-algorithms-fall-2011/lecture-videos/lecture-19-dynamic-programming-i-fibonacci-shortest-paths/)
* [MIT OCW - Dynamic Programming II](http://ocw.mit.edu/courses/electrical-engineering-and-computer-science/6-006-introduction-to-algorithms-fall-2011/lecture-videos/lecture-20-dynamic-programming-ii-text-justification-blackjack/)
* [MIT OCW - Dynamic Programming III](http://ocw.mit.edu/courses/electrical-engineering-and-computer-science/6-006-introduction-to-algorithms-fall-2011/lecture-videos/lecture-21-dp-iii-parenthesization-edit-distance-knapsack/)
* [MIT OCW - Dynamic Programming IV](http://ocw.mit.edu/courses/electrical-engineering-and-computer-science/6-006-introduction-to-algorithms-fall-2011/lecture-videos/lecture-22-dp-iv-guitar-fingering-tetris-super-mario-bros/)
* General class of algorithms which use a "careful brute force" technique.
* Basic idea: Split a problem into subproblems and reuse the subproblem solutions
* "Memoization": Process of recording subproblem solutions to be used later on
* DP = recursion + memoization (+ guessing)
* Running time = # of subproblems solved * time/subproblem
* Bottom-up approach
  * Start with simplest subproblems and work your way up to the more complex problem
  * Topological sort of subproblem dependency Directed Acyclic Graph (DAG)
  * "Once we formulate the solution to a problem recursively as in terms of its sub-problems, we can try reformulating the problem in a bottom-up fashion: try solving the sub-problems first and use their solutions to build-on and arrive at solutions to bigger sub-problems. This is also usually done in a tabular form by iteratively generating solutions to bigger and bigger sub-problems by using the solutions to small sub-problems."
* Top-down approach
  * "This is the direct fall-out of the recursive formulation of any problem. If the solution to any problem can be formulated recursively using the solution to its sub-problems, and if its sub-problems are overlapping, then one can easily memoize or store the solutions to the sub-problems in a table. Whenever we attempt to solve a new sub-problem, we first check the table to see if it is already solved. If a solution has been recorded, we can use it directly, otherwise we solve the sub-problem and add its solution to the table."
 
## Constraint Satisfaction Problems and Optimization
* "Constraint satisfaction problems (CSPs) are mathematical problems defined as a set of objects whose state must satisfy a number of constraints or limitations. CSPs represent the entities in a problem as a homogeneous collection of finite constraints over variables, which is solved by constraint satisfaction methods. CSPs are the subject of intense research in both artificial intelligence and operations research, since the regularity in their formulation provides a common basis to analyze and solve problems of many seemingly unrelated families. CSPs often exhibit high complexity, requiring a combination of heuristics and combinatorial search methods to be solved in a reasonable time." [[Wikipedia](https://en.wikipedia.org/wiki/Constraint_satisfaction_problem)]
* Optimization problems are a specialization of CSPs that find the best solution satisfying a set of constraints.
 * Linear programming is a further specialization in which we are trying to maximize a linear algebraic expression subject to linear constraints.
* Some examples of CSPs:
 * The N-queens problem (can be solved in "roughly linear time" using the min-conflicts algorithm)
 * Map coloring
 * Many logic puzzles (e.g. Sudoku)
