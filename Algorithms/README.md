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
* Performs an [in-order traversal](http://visualgo.net/bst) over a Binary Search Tree

| Worst Case            | Average Case | Best Case  | Worst Case (Space) |
|-----------------------|--------------|------------|--------------------|
| O(n log n) (balanced) | O(n log n)   | O(n log n) | Θ(n)               |

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
* TODO

## Knapsack
* TODO
