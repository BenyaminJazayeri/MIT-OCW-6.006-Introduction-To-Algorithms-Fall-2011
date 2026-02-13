# MIT-OCW-6.006-Introduction-To-Algorithms-Fall-2011

[![License: CC BY-NC-SA 4.0](https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc-sa/4.0/)

![logo](./logo.jpg)

My coursework for MIT OCW 6.006 Introduction To Algorithms Fall 2011 class. This covers the exact same coursework required of MIT students present in class for full marks.

All solutions are my own.

The Problem Set statements and their analytical solutions are available in the "Problem Set N Writeup.pdf" files. The corresponding code is in the accompanying source files.

For clarity, only created or edited code files are included.

Taught by [Prof. Erik Demaine](https://ocw.mit.edu/search/?q=Prof.+Erik+Demaine), [Prof. Srini Devadas](https://ocw.mit.edu/search/?q=Prof.+Srini+Devadas) and Recitation Instructor Victor Costan.

Course Homepage: https://ocw.mit.edu/courses/6-006-introduction-to-algorithms-fall-2011/

## Topics Covered

| Topic | Subtopics |
|-------|-----------|
| Sorting and Trees | Insertion sort, merge sort, heaps and heap sort, binary search trees, AVL trees, counting sort, radix sort, lower bounds for sorting |
| Hashing | Hashing with chaining, table doubling, Karp-Rabin, open addressing, cryptographic hashing |
| Numerics | Integer arithmetic, Karatsuba multiplication, square roots, Newton's method |
| Graphs | Breadth-first search, depth-first search, topological sorting |
| Shortest Paths | Single-source shortest paths, Dijkstra, Bellman-Ford |
| Dynamic Programming | Memoization, subproblems, text justification, edit distance, knapsack |
| Advanced Topics | P, NP, NP-completeness, reductions |

## Coursework Done

| Type | Count |
|------|-------|
| Problem Sets | 7 |
| Quizzes | 2 |
| Final Exam | 1 |

## Transcript

| Assessment | Grade |
|------------|-------|
| [Quiz 1](./Quiz%201) | 79/120* |
| [Quiz 2](./Quiz%202) | 102/120 |
| [Final Exam](./Final%20Exam) | 160/180 |

\*Quiz 1 scores were low across the board in the original Fall 2011 MIT class this course was recorded from. The course staff acknowledged this [here](https://youtu.be/a_otxyu0mSQ?si=FOkm1kT4oVYHMaTe&t=34): *"The results are lower than what we thought... the mistake was on our part."*

## Projects

### [Arbitrary-Precision Arithmetic Library for RSA](./Problem%20Set%205)
A complete big number arithmetic library implementing Karatsuba multiplication (O(n^log₂3)), Newton-Raphson division with inverse caching, and modular exponentiation (square-and-multiply). Uses hybrid dispatch, switching between asymptotically fast and brute-force algorithms based on input size. Applied to RSA public-key encryption and decryption.

### [BST / AVL / Range Tree + Sweep Line Circuit Layout](./Problem%20Set%203)
A full balanced tree hierarchy built from scratch: binary search tree with min-augmentation, AVL tree with rotations, and a size-augmented range tree supporting O(log n) rank and range queries. Used as the backing data structure for a sweep line algorithm that detects wire crossings in digital circuit layouts, replacing an O(n²) brute-force approach with O(n log n).

### [Dijkstra's Algorithm on the US Highway Network](./Problem%20Set%206)
Dijkstra's shortest-path algorithm applied to the National Highway Planning Network with great-circle distance and KML output for Google Earth visualization.

### [Rubik's Cube Bidirectional BFS Solver](./Problem%20Set%206)
A bidirectional BFS solver for the 2x2x2 Rubik's cube that explores from both start and goal states simultaneously, using permutation group inverses to reconstruct the solution path.

### [Content-Aware Image Resizing with Dynamic Programming (Seam Carving)](./Problem%20Set%207)
A dynamic programming implementation of the [Avidan & Shamir](https://www.youtube.com/watch?v=vIFCV2spKtg) seam carving algorithm. Computes the minimum-energy vertical seam using a bottom-up DP table with backpointers.

### [Min-Heap Priority Queue for Circuit Simulation](./Problem%20Set%202)
Profiled an event-driven circuit simulator, identified a bottleneck in the O(n) priority queue, and replaced it with a min-heap implementation built from scratch.

## My Other MIT Coursework

[18.01SC Single Variable Calculus](https://github.com/BenyaminJazayeri/MIT-OCW-18.01SC-Single-Variable-Calculus-Fall-2010)<br>
[18.02SC Multivariable Calculus](https://github.com/BenyaminJazayeri/MIT-OCW-18.02SC-Multivariable-Calculus-Fall-2010)<br>
[18.06SC Linear Algebra](https://github.com/BenyaminJazayeri/MIT-OCW-18.06SC-Linear-Algebra-Fall-2011)<br>
[6.0001 Intro to CS & Programming in Python](https://github.com/BenyaminJazayeri/MIT-OCW-6.0001-Introduction-To-Computer-Science-And-Programming-In-Python-Fall-2016)<br>
[6.0002 Intro to Computational Thinking & Data Science](https://github.com/BenyaminJazayeri/MIT-OCW-6.0002-Introduction-To-Computational-Thinking-And-Data-Science-Fall-2016)<br>
[6.034 Artificial Intelligence](https://github.com/BenyaminJazayeri/MIT-OCW-6.034-Artificial-Intelligence-Fall-2010)<br>
[6.036 Introduction to Machine Learning](https://github.com/BenyaminJazayeri/MIT-Open-Learning-6.036-Introduction-To-Machine-Learning-Spring-2019)<br>
[6.042J Mathematics for Computer Science](https://github.com/BenyaminJazayeri/MIT-OCW-6.042J-Mathematics-For-Computer-Science-Fall-2010)

I'd be very happy to discuss anything related to MIT OCW. Reach me at [benjamin.jazayeri@gmail.com](mailto:benjamin.jazayeri@gmail.com).
