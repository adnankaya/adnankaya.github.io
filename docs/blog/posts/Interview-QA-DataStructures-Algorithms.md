---
date:
  created: 2024-09-25
  updated: 2024-09-25
readtime: 10
pin: false
links:
  - Homepage: index.md#project-layout
  - Blog index: blog/index.md
  - External links:
    - Web Page: https://adnankaya.github.io
categories:
  - Junior
  - Interview
tags:
  - interview
  - junior
  - questions and answers
  - software developer
  - software engineering
  - junior developer
  - coding interview
  - programming interview
  - data structures
  - algorithms
authors:
  - adnankaya
slug: interview-questions-and-answers-data-structures-algorithms
---

# 100 Data Structures And Algorithms Interview Questions and Answers

Checkout our curated list of 100 interview questions and answers for data structures and algorithms.

<!-- more -->

???+ question "1. What is an array?"
    Answer: An array is a data structure that stores a fixed-size sequential collection of elements of the same type.
    It allows direct access to elements using their index, which makes it very efficient for retrieval. However, resizing an array can be expensive, as it may involve copying all elements to a new array. Arrays are used when the number of elements is known in advance, and fast retrieval is needed.

??? question "2. What is a linked list?"
    Answer: A linked list is a linear data structure where each element (called a node) points to the next node in the sequence.
    Unlike arrays, linked lists do not have fixed sizes and can grow dynamically. However, accessing elements requires traversal from the head node, making retrieval slower compared to arrays. Linked lists are useful when frequent insertions and deletions are needed.

??? question "3. What is the difference between an array and a linked list?"
    Answer: An array has fixed size and allows direct access to its elements, while a linked list is dynamic and elements can only be accessed sequentially.
    Arrays are better for fast access and random indexing, whereas linked lists are more efficient for frequent insertions and deletions.

??? question "4. What is a stack?"
    Answer: A stack is a data structure that follows the Last-In-First-Out (LIFO) principle, meaning the last element added is the first one to be removed.
    Stacks are commonly used for undo operations in text editors or for tracking function calls in recursion.

??? question "5. What is a queue?"
    Answer: A queue is a data structure that follows the First-In-First-Out (FIFO) principle, meaning the first element added is the first one to be removed.
    Queues are used in scheduling tasks, like printing jobs or managing tasks in an operating system.

??? question "6. What is a doubly linked list?"
    Answer: A doubly linked list is a type of linked list where each node contains references to both the next and the previous node.
    This allows traversal in both directions, making operations like insertion and deletion more flexible compared to singly linked lists, but it requires more memory due to the additional pointer.

??? question "7. What is a binary tree?"
    Answer: A binary tree is a hierarchical data structure where each node has at most two children, referred to as the left child and the right child.
    Binary trees are commonly used for searching and sorting algorithms, such as binary search trees, where the left child is less than the parent node and the right child is greater.

??? question "8. What is a binary search tree (BST)?"
    Answer: A binary search tree is a binary tree in which every node follows the rule: the left child is smaller than the parent, and the right child is larger.
    This property allows for efficient searching, insertion, and deletion operations, making it ideal for maintaining sorted data.

??? question "9. What is a graph?"
    Answer: A graph is a data structure consisting of nodes (vertices) and edges that connect pairs of nodes.
    Graphs can represent various real-world systems, such as social networks, where nodes are users and edges are friendships.

??? question "10. What is the difference between a tree and a graph?"
    Answer: A tree is a type of graph that has no cycles and has a hierarchical structure with a single root, whereas a graph can have cycles and may not be hierarchical.
    Trees are used in hierarchical data representation like file systems, while graphs can represent more complex relationships such as networks.

??? question "11. What is a heap?"
    Answer: A heap is a specialized binary tree-based data structure that satisfies the heap property: in a max heap, every parent node is greater than or equal to its children; in a min heap, every parent node is smaller than or equal to its children.
    Heaps are commonly used in priority queues and for sorting algorithms like Heap Sort.

??? question "12. What is a hash table?"
    Answer: A hash table is a data structure that maps keys to values using a hash function, allowing for fast data retrieval.
    Hash tables are often used for implementing associative arrays or dictionaries where fast lookup is important.

??? question "13. What is hashing?"
    Answer: Hashing is the process of converting input data into a fixed-size value using a hash function.
    It is used in hash tables to quickly locate data using a key, making operations like search, insert, and delete very efficient.

??? question "14. What is collision in hashing, and how is it handled?"
    Answer: A collision occurs when two different keys produce the same hash value.
    Collisions can be handled using techniques like chaining (storing multiple values in a bucket) or open addressing (finding the next available slot).

??? question "15. What is selection sort?"
    Answer: Selection sort is a simple comparison-based sorting algorithm that repeatedly selects the smallest element from the unsorted part of the list and swaps it with the first unsorted element.
    Although easy to understand, selection sort is inefficient for large datasets due to its time complexity of O(n^2).

??? question "16. What is bubble sort?"
    Answer: Bubble sort is a simple sorting algorithm that repeatedly steps through the list, compares adjacent elements, and swaps them if they are in the wrong order.
    It has a time complexity of O(n^2) and is generally considered inefficient for large datasets but is easy to implement.

??? question "17. What is merge sort?"
    Answer: Merge sort is a divide-and-conquer sorting algorithm that splits the list into halves, sorts each half recursively, and then merges them back together.
    With a time complexity of O(n log n), merge sort is more efficient than bubble or selection sort and works well for larger datasets.

??? question "18. What is quicksort?"
    Answer: Quicksort is a divide-and-conquer sorting algorithm that selects a pivot element and partitions the list into two sublists—one with elements smaller than the pivot and one with elements larger.
    Quicksort has an average time complexity of O(n log n) and is widely used due to its efficiency, though its worst-case time complexity is O(n^2).

??? question "19. What is linear search?"
    Answer: Linear search is a simple search algorithm that checks each element in a list one by one until the target element is found or the list ends.
    Its time complexity is O(n), making it inefficient for large datasets, but it's useful when the list is unsorted.

??? question "20. What is binary search?"
    Answer: Binary search is a search algorithm that works on sorted lists by repeatedly dividing the list in half and comparing the target value to the middle element.
    With a time complexity of O(log n), binary search is highly efficient but requires the list to be sorted before use.

??? question "21. What is an adjacency matrix in graph representation?"
    Answer: An adjacency matrix is a 2D array used to represent a graph, where each cell at position (i, j) indicates whether there is an edge between vertex i and vertex j.
    It is memory-efficient for dense graphs but consumes a lot of space for sparse graphs.

??? question "22. What is an adjacency list in graph representation?"
    Answer: An adjacency list represents a graph as a collection of lists, where each vertex has a list of the vertices it is connected to.
    This representation is more space-efficient than an adjacency matrix, especially for sparse graphs, and is widely used in practical applications.

??? question "23. What is breadth-first search (BFS)?"
    Answer: Breadth-first search is a graph traversal algorithm that starts at a given node and explores all its neighbors before moving to their neighbors.
    It is commonly used for finding the shortest path in unweighted graphs and can be implemented using a queue.

??? question "24. What is depth-first search (DFS)?"
    Answer: Depth-first search is a graph traversal algorithm that explores as far along a branch as possible before backtracking.
    It is implemented using a stack or recursion and is useful for applications like topological sorting and finding connected components.

??? question "25. What is the time complexity of breadth-first search (BFS)?"
    Answer: The time complexity of BFS is O(V + E), where V is the number of vertices and E is the number of edges in the graph.
    BFS visits every vertex and edge once, making it efficient for large graphs with relatively few edges.

??? question "26. What is the time complexity of depth-first search (DFS)?"
    Answer: The time complexity of DFS is O(V + E), where V is the number of vertices and E is the number of edges.
    Like BFS, DFS visits each vertex and edge once, making it suitable for deep exploration of graphs.

??? question "27. What is a priority queue?"
    Answer: A priority queue is a special type of queue where each element is associated with a priority, and elements with higher priority are dequeued before elements with lower priority.
    Priority queues are often implemented using heaps and are used in algorithms like Dijkstra's for finding the shortest path.

??? question "28. What is Dijkstra's algorithm?"
    Answer: Dijkstra's algorithm is a graph traversal algorithm used to find the shortest path from a starting node to all other nodes in a graph with non-negative edge weights.
    It uses a priority queue to ensure the shortest known distance is explored first, with a time complexity of O(V log V + E).

??? question "29. What is a balanced binary search tree?"
    Answer: A balanced binary search tree is a binary search tree where the height difference between the left and right subtrees of any node is at most one.
    This balance ensures that operations like search, insertion, and deletion are done in O(log n) time, improving performance compared to unbalanced trees.

??? question "30. What is an AVL tree?"
    Answer: An AVL tree is a self-balancing binary search tree where the height of two child subtrees of any node differs by at most one.
    It maintains balance through tree rotations, ensuring O(log n) time complexity for operations like search, insert, and delete.

??? question "31. What is a Red-Black tree?"
    Answer: A Red-Black tree is a type of self-balancing binary search tree where each node has an additional color attribute (red or black) to maintain balance.
    Red-Black trees guarantee O(log n) time complexity for insertions, deletions, and lookups, and are widely used in many libraries and databases.

??? question "32. What is hashing with chaining?"
    Answer: Hashing with chaining is a technique for handling collisions in a hash table where each bucket points to a linked list of key-value pairs.
    This method allows multiple elements to be stored in the same bucket, reducing the chances of collision but potentially increasing the time complexity of search operations in a worst-case scenario.

??? question "33. What is hashing with open addressing?"
    Answer: Hashing with open addressing is a method for handling collisions where, upon a collision, the algorithm looks for the next available slot in the table to place the new element.
    Techniques like linear probing and quadratic probing are used to find the next slot, but it can lead to clustering issues in some cases.

??? question "34. What is Kruskal’s algorithm?"
    Answer: Kruskal’s algorithm is a greedy algorithm used to find the minimum spanning tree of a graph by sorting edges and adding them one by one to the tree while avoiding cycles.
    It has a time complexity of O(E log E) and is widely used in network design and clustering problems.

??? question "35. What is Prim’s algorithm?"
    Answer: Prim’s algorithm is a greedy algorithm used to find the minimum spanning tree of a graph by starting from any node and adding the smallest edge that connects a new vertex to the tree.
    Like Kruskal’s algorithm, it ensures all vertices are connected with the minimum possible total edge weight, and its time complexity is O(V^2) with an adjacency matrix or O(E log V) with a priority queue.

??? question "36. What is dynamic programming?"
    Answer: Dynamic programming is an optimization technique used to solve problems by breaking them down into overlapping subproblems, storing their results to avoid redundant computation.
    It is useful for problems like the Fibonacci sequence and shortest path algorithms, where recomputing solutions to subproblems is inefficient.

??? question "37. What is memoization in dynamic programming?"
    Answer: Memoization is a technique where the results of expensive function calls are cached so they do not need to be recalculated when the same inputs occur again.
    This is commonly used in dynamic programming to optimize recursive algorithms by storing previously computed results.

??? question "38. What is the difference between dynamic programming and greedy algorithms?"
    Answer: Dynamic programming solves problems by breaking them into subproblems and solving each subproblem just once, whereas greedy algorithms make a series of choices that seem locally optimal at each step.
    Greedy algorithms may not always produce the optimal solution, while dynamic programming guarantees an optimal solution when applicable.

??? question "39. What is a topological sort?"
    Answer: A topological sort is a linear ordering of vertices in a directed acyclic graph such that for every directed edge u -> v, vertex u appears before vertex v in the ordering.
    Topological sorting is used in scenarios like task scheduling where some tasks must be done before others.

??? question "40. What is a trie?"
    Answer: A trie (or prefix tree) is a tree-like data structure used to store strings, where each node represents a character of the string.
    It is commonly used in autocomplete systems and dictionaries for efficient retrieval of string prefixes, providing fast search, insert, and delete operations.

??? question "41. What is the difference between a directed and an undirected graph?"
    Answer: In a directed graph, edges have a direction, meaning they go from one vertex to another and not the reverse. In an undirected graph, edges do not have a direction and connect vertices bidirectionally.
    Directed graphs are used for one-way relationships like web links, while undirected graphs represent bidirectional relationships like friendships on social networks.

??? question "42. What is a spanning tree?"
    Answer: A spanning tree of a graph is a subgraph that includes all the vertices of the original graph and forms a tree, meaning it is connected and has no cycles.
    Spanning trees are used in network design and optimization problems where we need to ensure all nodes are connected with minimal connections.

??? question "43. What is a binary heap?"
    Answer: A binary heap is a complete binary tree that maintains a specific order property where the parent node is either greater than or smaller than its children, depending on whether it's a max-heap or min-heap.
    Binary heaps are often used to implement priority queues and for algorithms like heapsort.

??? question "44. How does heapsort work?"
    Answer: Heapsort is a comparison-based sorting algorithm that uses a binary heap data structure to sort an array. It first builds a max-heap and then repeatedly extracts the maximum element, placing it at the end of the array.
    The time complexity of heapsort is O(n log n), and it is an in-place sorting algorithm.

??? question "45. What is the difference between a binary search tree and a binary heap?"
    Answer: A binary search tree (BST) maintains a sorted order where left child nodes are smaller, and right child nodes are greater than the parent node. A binary heap, on the other hand, ensures that each parent node is either greater or smaller than its children, but it doesn't enforce any ordering between siblings.
    BSTs are used for efficient searching, while binary heaps are used in priority queues.

??? question "46. What is a splay tree?"
    Answer: A splay tree is a self-adjusting binary search tree that moves frequently accessed elements closer to the root, optimizing future accesses.
    It is used in scenarios where some elements are accessed more frequently than others, providing amortized O(log n) access time.

??? question "47. What is a B-tree?"
    Answer: A B-tree is a self-balancing search tree in which nodes can have multiple children. It is used to keep data sorted and allow for searches, sequential access, insertions, and deletions in logarithmic time.
    B-trees are commonly used in databases and file systems to efficiently manage large amounts of sorted data that cannot fit in memory.

??? question "48. What is the difference between a B-tree and a binary search tree?"
    Answer: A binary search tree (BST) has nodes with at most two children, while a B-tree can have multiple children per node, making it more suitable for handling large amounts of data.
    B-trees are optimized for disk storage and are used in databases, whereas binary search trees are usually used for in-memory data structures.

??? question "49. What is Floyd-Warshall algorithm?"
    Answer: The Floyd-Warshall algorithm is an algorithm for finding the shortest paths between all pairs of vertices in a weighted graph.
    It uses dynamic programming to calculate paths and has a time complexity of O(V^3), making it suitable for dense graphs but inefficient for sparse graphs.

??? question "50. What is the Bellman-Ford algorithm?"
    Answer: The Bellman-Ford algorithm is a graph traversal algorithm used to find the shortest paths from a single source vertex to all other vertices in a weighted graph, even with negative weights.
    It is slower than Dijkstra’s algorithm with a time complexity of O(V * E), but it can handle negative weight edges, unlike Dijkstra.

??? question "51. What is a connected graph?"
    Answer: A graph is connected if there is a path between every pair of vertices.
    In a connected graph, all nodes can be reached from any other node, which is crucial in network design to ensure communication between all parts of a system.

??? question "52. What is a strongly connected component?"
    Answer: In a directed graph, a strongly connected component is a subgraph where every vertex is reachable from every other vertex.
    Strongly connected components are useful in analyzing directed networks like the web, where some parts are tightly interlinked.

??? question "53. What is a top-down approach in dynamic programming?"
    Answer: The top-down approach in dynamic programming involves solving the problem by recursively breaking it down into smaller subproblems and caching their results (memoization).
    This approach is useful when the recursive structure of the problem is clear, and you want to avoid recalculating the same results multiple times.

??? question "54. What is a bottom-up approach in dynamic programming?"
    Answer: The bottom-up approach in dynamic programming solves smaller subproblems first and builds up the solution to the main problem iteratively.
    This approach is often more space-efficient than the top-down approach and avoids the overhead of recursion.

??? question "55. What is KMP algorithm?"
    Answer: The Knuth-Morris-Pratt (KMP) algorithm is an efficient string searching algorithm that avoids redundant comparisons by using a partial match table (or prefix table) to skip sections of the text.
    It has a time complexity of O(n + m), where n is the length of the text and m is the length of the pattern, making it faster than the naive search algorithm.

??? question "56. What is Rabin-Karp algorithm?"
    Answer: The Rabin-Karp algorithm is a string searching algorithm that uses hashing to find a substring within a text. It calculates a hash for the pattern and compares it to the hash of substrings in the text.
    It has an average time complexity of O(n), but in the worst case, when hash collisions occur, it can degrade to O(n * m).

??? question "57. What is amortized analysis?"
    Answer: Amortized analysis is used to analyze the average time complexity of an operation over a sequence of operations, rather than a single operation.
    It is useful for data structures like dynamic arrays and splay trees, where occasional costly operations are balanced out by many cheaper operations.

??? question "58. What is the sliding window technique?"
    Answer: The sliding window technique involves maintaining a subset of data as a "window" and moving it across the input to solve problems like finding maximum sums or subarrays of a certain length.
    This technique optimizes problems involving sequences and is often used in dynamic programming or array manipulation.

??? question "59. What is a union-find data structure?"
    Answer: A union-find (or disjoint-set) data structure is used to keep track of a set of elements partitioned into disjoint subsets. It supports two operations: union, which merges two sets, and find, which finds the representative of a set.
    It is used in Kruskal’s algorithm and other applications involving connectivity, with an amortized time complexity of nearly constant time using path compression and union by rank.

??? question "60. What is the master theorem?"
    Answer: The master theorem provides a formula to determine the time complexity of divide-and-conquer algorithms, especially recurrence relations.
    It simplifies the analysis of algorithms like mergesort and quicksort, allowing for easy calculation of time complexity without solving the recurrence from scratch.

??? question "61. What is a graph traversal?"
    Answer: Graph traversal is the process of visiting all the nodes (or vertices) in a graph. The two most common methods are Breadth-First Search (BFS) and Depth-First Search (DFS).
    Graph traversal is used in many applications, such as searching the web or finding the shortest path in navigation systems.

??? question "62. How does Breadth-First Search (BFS) work?"
    Answer: BFS starts at a source node and explores all its neighboring nodes level by level before moving to the next level. It uses a queue to keep track of the nodes to visit.
    BFS is used when we want to find the shortest path in an unweighted graph or explore all nodes within a certain "distance" from the source.

??? question "63. How does Depth-First Search (DFS) work?"
    Answer: DFS explores as far as possible along each branch before backtracking, using a stack or recursion to manage the traversal.
    DFS is useful for problems that require searching all possible paths or discovering connected components in a graph.

??? question "64. What is the time complexity of BFS and DFS?"
    Answer: The time complexity of both BFS and DFS is O(V + E), where V is the number of vertices and E is the number of edges in the graph.
    This is because each algorithm must visit every vertex and edge once in the worst case.

??? question "65. What is a cycle in a graph?"
    Answer: A cycle is a path in a graph where the starting and ending vertices are the same, and no edges or vertices (except the starting/ending vertex) are repeated.
    Detecting cycles is important in applications like dependency resolution in package managers and deadlock detection.

??? question "66. How can you detect a cycle in a graph?"
    Answer: In an undirected graph, a cycle can be detected using BFS or DFS by checking if a visited node is revisited during traversal, except for its immediate parent. In a directed graph, cycle detection can be done using DFS with recursion and a stack to track the visited nodes.
    Detecting cycles is important to avoid infinite loops in algorithms or processes.

??? question "67. What is topological sorting?"
    Answer: Topological sorting is the linear ordering of vertices in a directed acyclic graph (DAG) such that for every directed edge from vertex u to vertex v, u comes before v in the ordering.
    It is used in scenarios like task scheduling, where certain tasks must be completed before others.

??? question "68. How do you perform topological sorting?"
    Answer: Topological sorting can be performed using DFS, where nodes are pushed onto a stack after all their descendants are processed. Alternatively, Kahn’s algorithm uses BFS by repeatedly removing nodes with no incoming edges.
    Topological sorting is used in dependency resolution, such as in build systems or course prerequisites.

??? question "69. What is a strongly connected graph?"
    Answer: A strongly connected graph is a directed graph in which every pair of vertices is reachable from each other.
    Strongly connected graphs are important in social network analysis to identify tightly knit communities where every member is directly or indirectly connected to every other member.

??? question "70. What is a minimum spanning tree (MST)?"
    Answer: A minimum spanning tree is a subset of a graph that connects all vertices with the smallest possible total edge weight and contains no cycles.
    MSTs are used in network design, such as minimizing the cost of laying cables between cities or constructing water pipelines.

??? question "71. What is Kruskal’s algorithm?"
    Answer: Kruskal’s algorithm is a greedy algorithm for finding the minimum spanning tree of a graph. It repeatedly adds the smallest edge to the tree, as long as it doesn’t form a cycle, until all vertices are connected.
    It is efficient for sparse graphs and uses the union-find data structure to detect cycles.

??? question "72. What is Prim’s algorithm?"
    Answer: Prim’s algorithm is a greedy algorithm that grows the minimum spanning tree from a starting vertex by adding the smallest edge connecting the tree to a vertex not yet in the tree.
    It is efficient for dense graphs and can be implemented using a priority queue.

??? question "73. What is Dijkstra’s algorithm?"
    Answer: Dijkstra’s algorithm finds the shortest path from a source node to all other nodes in a graph with non-negative edge weights. It works by iteratively selecting the closest unvisited node and updating the distances to its neighbors.
    Dijkstra’s algorithm is widely used in routing and navigation systems to find the shortest route between locations.

??? question "74. What is a self-balancing binary search tree?"
    Answer: A self-balancing binary search tree automatically keeps its height balanced after insertions and deletions, ensuring that operations like search, insert, and delete are done in O(log n) time. Examples include AVL trees and Red-Black trees.
    These trees are used in applications where efficient lookups and updates are crucial, such as in databases or file systems.

??? question "75. What is an AVL tree?"
    Answer: An AVL tree is a self-balancing binary search tree where the height difference (balance factor) between the left and right subtrees of any node is at most 1.
    AVL trees provide O(log n) search, insertion, and deletion operations, making them suitable for applications requiring frequent lookups.

??? question "76. What is a Red-Black tree?"
    Answer: A Red-Black tree is a self-balancing binary search tree where nodes are colored either red or black, and certain properties (e.g., no two red nodes can be adjacent) ensure that the tree remains balanced.
    Red-Black trees offer O(log n) time complexity for search, insert, and delete, and are commonly used in standard library implementations like `std::map` and `std::set` in C++.

??? question "77. What is a trie?"
    Answer: A trie, or prefix tree, is a tree-like data structure used to store a dynamic set of strings where each node represents a single character of a word. It allows for fast searching, especially for prefix-based queries.
    Tries are commonly used in autocomplete systems and spell checkers.

??? question "78. What is a suffix tree?"
    Answer: A suffix tree is a compressed trie that stores all the suffixes of a given string. It allows for efficient pattern matching, substring search, and longest common substring queries.
    Suffix trees are used in DNA sequence analysis and text processing.

??? question "79. What is a bloom filter?"
    Answer: A bloom filter is a probabilistic data structure used to test whether an element is part of a set. It uses multiple hash functions and bit arrays but allows for false positives (though no false negatives).
    Bloom filters are useful in situations where memory is limited, such as in network caching or databases.

??? question "80. What is dynamic programming?"
    Answer: Dynamic programming is a method of solving complex problems by breaking them down into simpler overlapping subproblems and storing the results of these subproblems to avoid redundant work.
    It is commonly used in optimization problems, such as calculating the shortest path in a graph or solving the knapsack problem.

??? question "81. What is memoization in dynamic programming?"
    Answer: Memoization is an optimization technique used in dynamic programming to store the results of expensive function calls and reuse them when the same inputs occur again, preventing redundant calculations.
    This technique is useful in recursive algorithms, such as computing Fibonacci numbers or solving the knapsack problem, where subproblems overlap.

??? question "82. What is a greedy algorithm?"
    Answer: A greedy algorithm makes a series of choices, each of which looks the best at the moment, in the hope that these local choices lead to a globally optimal solution.
    Greedy algorithms are used in problems like activity selection and Huffman coding. However, they don’t always guarantee an optimal solution for all problems.

??? question "83. What is a divide-and-conquer algorithm?"
    Answer: Divide-and-conquer is a strategy where a problem is divided into smaller subproblems, each solved independently, and then combined to form the final solution.
    Merge sort and quicksort are classic examples of divide-and-conquer algorithms.

??? question "84. How does the quicksort algorithm work?"
    Answer: Quicksort is a divide-and-conquer sorting algorithm that selects a "pivot" element, partitions the array into two sub-arrays (one with elements smaller than the pivot, the other larger), and recursively sorts the sub-arrays.
    It has an average time complexity of O(n log n), but in the worst case (e.g., if the pivot is always the smallest element), it can degrade to O(n²).

??? question "85. How does the merge sort algorithm work?"
    Answer: Merge sort is a divide-and-conquer algorithm that recursively divides the array in half, sorts each half, and then merges the sorted halves into a complete sorted array.
    Merge sort guarantees O(n log n) time complexity and is stable, meaning it preserves the relative order of equal elements.

??? question "86. What is the time complexity of dynamic programming solutions?"
    Answer: The time complexity of dynamic programming depends on the number of subproblems and the time taken to solve each subproblem. Generally, it reduces the complexity of recursive solutions by turning them into polynomial time, often O(n²) or O(n).
    For example, solving the Fibonacci sequence with dynamic programming reduces the complexity from exponential O(2^n) to linear O(n).

??? question "87. What is backtracking?"
    Answer: Backtracking is a general algorithmic technique that builds a solution incrementally, abandoning a solution path as soon as it determines that the path cannot lead to a valid solution.
    It is used in constraint satisfaction problems such as solving Sudoku, the N-Queens problem, or generating permutations.

??? question "88. What is hashing?"
    Answer: Hashing is a technique for mapping data (such as a string or number) to a fixed-size value using a hash function. The resulting hash value is then used to store or retrieve data efficiently in constant time O(1).
    Hash tables use this principle and are commonly used for fast lookups, such as in dictionaries or caches.

??? question "89. What is a hash collision and how can it be resolved?"
    Answer: A hash collision occurs when two different inputs produce the same hash value. Common methods to resolve collisions include chaining (storing elements with the same hash value in a linked list) and open addressing (finding another location in the array using probing).
    Efficient collision handling is critical to maintaining the O(1) performance of hash tables.

??? question "90. What is double hashing?"
    Answer: Double hashing is a collision resolution method that applies a second hash function when a collision occurs. The second hash function generates a step size that is used to probe for the next available slot.
    It helps reduce clustering in open addressing by ensuring that subsequent probes are spread out more evenly.

??? question "91. What is a priority queue?"
    Answer: A priority queue is an abstract data type where each element has a priority, and elements are served based on their priority rather than their order of insertion. The highest (or lowest) priority element is dequeued first.
    Priority queues are often implemented using heaps and are used in algorithms like Dijkstra’s shortest path and Huffman coding.

??? question "92. What is a binary heap?"
    Answer: A binary heap is a complete binary tree where each parent node is either greater than or equal to (max-heap) or less than or equal to (min-heap) its children. Binary heaps are commonly used to implement priority queues.
    Binary heaps allow for efficient insertion, deletion, and retrieval of the minimum (or maximum) element in O(log n) time.

??? question "93. How is a binary heap implemented?"
    Answer: A binary heap is typically implemented as an array, where for any element at index i, its left child is at index 2i+1 and its right child is at index 2i+2. Heap operations maintain the heap property by "bubbling up" or "bubbling down" elements as needed.
    This structure is used in algorithms like heap sort and in implementing priority queues.

??? question "94. What is heap sort?"
    Answer: Heap sort is a comparison-based sorting algorithm that uses a binary heap. It first builds a max-heap from the array, and then repeatedly extracts the largest element from the heap and places it at the end of the array.
    Heap sort has a time complexity of O(n log n) and is in-place, but it is not stable.

??? question "95. What is amortized time complexity?"
    Answer: Amortized time complexity is the average time per operation over a sequence of operations, even if some individual operations take longer than others. It is used when analyzing operations that can have occasional high costs but are generally efficient.
    Examples include dynamic array resizing and certain operations in splay trees and disjoint sets.

??? question "96. What is a disjoint set?"
    Answer: A disjoint set, also known as a union-find data structure, keeps track of a set of elements partitioned into non-overlapping subsets. It supports two main operations: union (merging two sets) and find (determining the set to which an element belongs).
    Disjoint sets are used in algorithms for finding connected components in a graph and Kruskal's algorithm for minimum spanning trees.

??? question "97. How do union and find operations work in a disjoint set?"
    Answer: The find operation locates the root of the set containing a given element, while the union operation merges two sets by linking one root to another. Techniques like path compression and union by rank optimize these operations to nearly constant time.
    These optimizations make disjoint sets highly efficient in practice.

??? question "98. What is Floyd-Warshall algorithm?"
    Answer: Floyd-Warshall is an algorithm for finding the shortest paths between all pairs of nodes in a weighted graph. It uses dynamic programming to iteratively improve the path between every pair of nodes by considering each node as an intermediate.
    It is especially useful in dense graphs and has a time complexity of O(n³).

??? question "99. What is Bellman-Ford algorithm?"
    Answer: The Bellman-Ford algorithm computes the shortest paths from a single source node to all other nodes in a weighted graph, even if some edge weights are negative. It works by iteratively relaxing all edges until no more improvements can be made.
    Bellman-Ford can detect negative weight cycles and has a time complexity of O(V * E).

??? question "100. What is a suffix array?"
    Answer: A suffix array is a sorted array of all suffixes of a string. It is a space-efficient alternative to a suffix tree and is used in string matching, data compression, and bioinformatics.
    Suffix arrays allow for efficient searching of patterns in large texts, with a time complexity of O(m + log n), where m is the pattern length and n is the text length.
