# Assignment 3: Understanding Algorithm Efficiency and Scalability
## Overview
This repository contains the implementation and analysis of two important algorithms:
1. **Randomized Quicksort**
2. **Hashing with Chaining**
The objective of this assignment is to understand algorithm efficiency, scalability, and how algorithm design choices impact performance. This project includes Python implementations, experimental comparisons, and a detailed report containing theoretical analysis and performance evaluation.
## Repository Contents
Assignment-3/
├──  Randomized Quicksort Analysis.ipynb # Randomized Quicksort and  Deterministic Quicksort implementation and comparison
├── Hashing with Chaining.ipynb  # Hash table implementation using chaining
├── Analysis_Report.pdf            # Detailed theoretical and empirical analysis
└── README.md                      # Project documentation
# Part 1: Randomized Quicksort
## Implementation
Randomized Quicksort is implemented by selecting the pivot element uniformly at random from the current subarray during every recursive call.
The implementation handles different input conditions, including:
- Randomly generated arrays
- Already sorted arrays
- Reverse-sorted arrays
- Arrays containing repeated elements
- Empty arrays
- Single-element arrays
The algorithm is also compared with Deterministic Quicksort, where the first element is always selected as the pivot.
## Analysis Summary
The expected average-case time complexity of Randomized Quicksort is:
O(n log n)
The random selection of pivots significantly reduces the probability of repeatedly selecting poor pivots that create highly unbalanced partitions.
The theoretical analysis using recurrence relations and indicator random variables demonstrates that the expected number of comparisons performed by Randomized Quicksort grows proportionally to:
n log n
Although the worst-case running time can still reach:
O(n²)
the probability of consistently choosing the worst possible pivot throughout the recursion is extremely small.
# Part 2: Hashing with Chaining
## Implementation
A hash table using chaining for collision resolution is implemented. The hash table supports the following operations:
- Insert key-value pairs
- Search values using keys
- Delete key-value pairs
The implementation uses a hash function to distribute keys across available buckets. When multiple keys map to the same bucket, chaining is used to store multiple elements while maintaining efficient access.
## Analysis Summary
Under the assumption of simple uniform hashing, the expected time complexity of hash table operations is:
Operation	Expected Time Complexity
Insert   	O(1 + α)
Search   	O(1 + α)
Delete   	O(1 + α)
where:
α = n / m
represents the load factor of the hash table.
By maintaining a low load factor through techniques such as dynamic resizing, the expected performance of insert, search, and delete operations becomes:
O(1)

# Running the Project
## Requirements
- Python 3.x installed
- No additional external libraries are required unless specified
## Run Randomized Quicksort
python Randomized Quicksort Analysis.ipynb

## Run Hash Table with Chaining
python Hashing with Chaining.ipynb

# Experimental Results Summary
The experiments demonstrate the following findings:
- Randomized Quicksort provides consistent performance across different input distributions because random pivot selection prevents repeated poor partitioning.
- Deterministic Quicksort performs poorly on already sorted and reverse-sorted arrays because selecting the first element as the pivot can create highly unbalanced partitions.
- Randomized Quicksort achieves expected average-case performance of O(n log n).
- Hashing with Chaining provides efficient insertion, searching, and deletion operations.
- Maintaining a lower load factor reduces collisions, shortens chains, and improves overall hash table performance.
# Conclusion
This project demonstrates the importance of algorithm selection and design decisions when analyzing efficiency and scalability.
Randomized Quicksort improves reliability by reducing the chance of worst-case partitioning, while Hashing with Chaining provides efficient data retrieval through effective collision handling.
The complete theoretical analysis, recurrence relation analysis, indicator random variable analysis, and experimental results are provided in the accompanying analysis report.
# Author
**Murali Krishna Vattikunta **  
Course: Algorithms and Data Structures (MSCS-532-B01) - Second Bi-term
Assignment: Understanding Algorithm Efficiency and Scalability

<img width="468" height="653" alt="image" src="https://github.com/user-attachments/assets/6468847c-7712-45a8-9287-f5537fc699c2" />
