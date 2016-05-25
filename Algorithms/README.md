# Algorithms

## Algorithm Analysis
* [Khan Academy - Asymptotic Notation](https://www.khanacademy.org/computing/computer-science/algorithms/asymptotic-notation/a/asymptotic-notation)
* [Wikipedia - Analysis of Algorithms](https://en.wikipedia.org/wiki/Analysis_of_algorithms)
* [A Gentle Introduction to Algorithm Complexity](http://discrete.gr/complexity/)
* [Princeton - An Introdution to the Analysis of Algorithms](http://aofa.cs.princeton.edu/home/)

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

### Mergesort
  * Requires more memory than Quicksort, but is faster in the worst case

| Worst Case | Average Cast | Best Case                               | Worse Case (Space) |
|------------|--------------|-----------------------------------------|--------------------|
| O(n log n) | O(n log n)   | O(n log n) typical,O(n) natural variant | O(n)               |

### Quicksort
 * [Wikipedia Article on Quicksort](https://en.wikipedia.org/wiki/Quicksort)
 * "Typically, quicksort is significantly faster in practice than other Θ(nlogn) algorithms, because its inner loop can be efficiently implemented on most architectures, and in most real-world data, it is possible to make design choices which minimize the probability of requiring quadratic time."
 * Low memory requirement

| Worst Case       | Average Cast | Best Case          | Worse Case (Space)       |
|------------------|--------------|--------------------|--------------------------|
| O(n<sup>2</sup>) | O(n log n)   | O(n log n) or O(n) | O(n) (naive) or O(log n) |

### Heapsort

### BST Sort

## Searching / Graph Traversal
* Binary Search
* Breadth-First
* Depth-First
* Uniform-Cost/Dijkstra's
* A*
