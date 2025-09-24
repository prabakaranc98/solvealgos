# Design and Analysis of Algorithms - Master Midterm Preparation Guide

## 📚 Core Resources & References

### Primary Textbook
- **CLRS**: Introduction to Algorithms (4th Edition) - Cormen, Leiserson, Rivest, Stein
  - [MIT Press Official Page](https://mitpress.mit.edu/9780262046305/introduction-to-algorithms/)

### Essential Online Resources
- [MIT 6.006 Introduction to Algorithms](https://ocw.mit.edu/courses/6-006-introduction-to-algorithms-fall-2011/)
- [MIT 6.046J Design and Analysis of Algorithms](https://ocw.mit.edu/courses/6-046j-design-and-analysis-of-algorithms-spring-2015/)
- [Stanford CS161: Design and Analysis of Algorithms](https://web.stanford.edu/class/cs161/)
- [CMU 15-451/651: Algorithm Design and Analysis](https://www.cs.cmu.edu/~15451/)
- [Princeton COS 423: Theory of Algorithms](https://www.cs.princeton.edu/courses/archive/fall20/cos423/)
- [UIUC CS 374: Algorithms & Models of Computation](https://courses.engr.illinois.edu/cs374/)

---

## ✅ Master Preparation Checklist

### Week 1: Foundations & Sorting

#### □ **Insertion Sort** (CLRS Ch. 2.1-2.2)
- [ ] Understand loop invariants and correctness proof
- [ ] Analyze best, worst, and average case complexity
- [ ] Implement from scratch without reference
- [ ] Practice: Problems 2-1, 2-2, 2-3, 2-4 from CLRS

#### □ **Asymptotic Notation** (CLRS Ch. 3)
- [ ] Master Big-O, Ω, Θ, o, ω notations
- [ ] Prove relationships using limit definitions
- [ ] Practice simplifying complex expressions
- [ ] Memorize common function growth rates
- [ ] Key theorems: Stirling's approximation, logarithm properties

#### □ **Divide & Conquer Paradigm** (CLRS Ch. 2.3, 4.1)
- [ ] Understand the three-step process
- [ ] Identify when to apply divide & conquer
- [ ] Practice writing recurrence relations

### Week 2: Advanced Sorting & Recurrences

#### □ **Mergesort** (CLRS Ch. 2.3, 4.0, 4.4)
- [ ] Prove correctness using induction
- [ ] Analyze space complexity (in-place vs. standard)
- [ ] Implement iterative version
- [ ] Count inversions variation

#### □ **Recurrence Relations** (CLRS Ch. 4)
- [ ] **Substitution Method**: Practice guessing and proving bounds
- [ ] **Recursion Trees**: Draw trees for T(n) = aT(n/b) + f(n)
- [ ] **Master Theorem**: Memorize all three cases
  - Case 1: f(n) = O(n^(log_b(a) - ε))
  - Case 2: f(n) = Θ(n^(log_b(a)) * log^k(n))
  - Case 3: f(n) = Ω(n^(log_b(a) + ε))
- [ ] Practice extended Master Theorem variations

#### □ **Binary Search** (CLRS Ch. 2.3 exercises)
- [ ] Implement recursive and iterative versions
- [ ] Prove correctness with loop invariants
- [ ] Variations: first/last occurrence, rotated arrays

### Week 3: Randomized Algorithms

#### □ **Quicksort** (CLRS Ch. 7)
- [ ] Deterministic version analysis
- [ ] Randomized version expected time analysis
- [ ] Partitioning schemes (Lomuto vs. Hoare)
- [ ] Worst-case construction
- [ ] Tail recursion optimization

#### □ **Probability Fundamentals** (CLRS Appendix C, Ch. 5)
- [ ] **Indicator Random Variables**: Definition and applications
- [ ] **Linearity of Expectation**: Non-independent case proofs
- [ ] **Birthday Paradox**: Derive the formula
- [ ] **Balls and Bins**: Expected maximum load
- [ ] **Coupon Collector's Problem**: Complete analysis

#### □ **Strassen's Algorithm** (CLRS Ch. 4.2)
- [ ] Understand the 7 multiplications trick
- [ ] Analyze crossover point with standard multiplication
- [ ] Numerical stability issues

### Week 4: Graph Algorithms

#### □ **Graph Representations** (CLRS Ch. 22.1, Appendix B.4-B.5)
- [ ] Adjacency matrix vs. adjacency list trade-offs
- [ ] Space/time complexity for common operations
- [ ] Conversion between representations

#### □ **Breadth-First Search (BFS)** (CLRS Ch. 22.2)
- [ ] Prove correctness of shortest path property
- [ ] BFS tree properties
- [ ] Applications:
  - [ ] Shortest paths in unweighted graphs
  - [ ] Testing bipartiteness
  - [ ] Finding connected components
  - [ ] Level-order traversal

#### □ **Depth-First Search (DFS)** (CLRS Ch. 22.3)
- [ ] Understand timestamps (discovery/finish)
- [ ] Parenthesis theorem
- [ ] White-path theorem
- [ ] Edge classification (tree, back, forward, cross)

#### □ **Topological Sort** (CLRS Ch. 22.4)
- [ ] DFS-based algorithm
- [ ] Kahn's algorithm (BFS-based)
- [ ] Proof of correctness
- [ ] Detecting cycles

#### □ **Strongly Connected Components** (CLRS Ch. 22.5)
- [ ] Kosaraju's algorithm
- [ ] Tarjan's algorithm (optional)
- [ ] Component graph properties

---

## 🎯 30 Core Practice Problems (Medium-Hard)

### Sorting & Divide-Conquer (Problems 1-8)

1. **Inversion Count Variants**: Given array A, find the number of triplets (i,j,k) where i<j<k and A[i]>A[j]>A[k]. Design O(n²log n) algorithm.

2. **K-way Merge**: Merge k sorted arrays of total n elements. Analyze using both min-heap and divide-conquer approaches.

3. **Nuts and Bolts**: Match n nuts to n bolts where you can only compare nuts with bolts. Design randomized O(n log n) expected time algorithm.

4. **Modified Quicksort**: Design a quicksort variant that switches to insertion sort for subarrays smaller than k. Find optimal k analytically.

5. **Counting Range**: Given sorted array and multiple queries [L,R], count elements in range efficiently after O(n log n) preprocessing.

6. **Closest Pair 3D**: Extend the 2D closest pair algorithm to 3D points. Maintain O(n log n) complexity.

7. **Maximum Subarray Variants**: Find maximum sum subarray with at most k elements. Design O(nk) algorithm.

8. **Pancake Sorting**: Sort array using only "flip" operations (reverse prefix). Analyze your algorithm's flip count.

### Recurrences & Analysis (Problems 9-15)

9. **Complex Recurrence**: Solve T(n) = 2T(n/3) + T(n/2) + n² using recursion tree method.

10. **Variable Split**: Analyze T(n) = T(αn) + T((1-α)n) + n where 0<α<1 is constant.

11. **Log Factor**: Solve T(n) = 3T(n/2) + n log n. Why doesn't Master Theorem directly apply?

12. **Akra-Bazzi Application**: T(n) = T(n/2) + T(n/3) + T(n/6) + n

13. **Space-Time Tradeoff**: Algorithm A: T(n)=2T(n/2)+n, S(n)=O(n). Algorithm B: T(n)=T(n/2)+n², S(n)=O(1). When to use each?

14. **Amortized Analysis**: Analyze a stack with multipop operation using accounting method.

15. **Recursion Depth**: Prove maximum recursion depth for randomized quicksort is O(log n) with high probability.

### Randomization & Probability (Problems 16-22)

16. **Randomized Selection**: Analyze the expected number of comparisons for finding the median using randomized selection.

17. **Skip Lists**: Prove expected search time is O(log n) and expected space is O(n).

18. **Reservoir Sampling**: Select k items uniformly from stream of unknown length n. Prove correctness.

19. **Min-Cut**: Analyze Karger's randomized min-cut algorithm success probability.

20. **Load Balancing**: n balls into n bins randomly. Prove max load is O(log n/log log n) with high probability.

21. **Randomized Rounding**: Use randomized rounding for MAX-SAT approximation.

22. **Treaps**: Analyze expected height of treap with n nodes.

### Graphs (Problems 23-30)

23. **BFS Tree Diameter**: Prove the diameter of BFS tree from any vertex is at most twice the graph diameter.

24. **Cycle Detection**: Find shortest cycle containing a given edge in O(V+E) time.

25. **Bipartite Matching**: Check if a bipartite graph has a perfect matching using BFS/DFS.

26. **Bridge Finding**: Find all bridges in undirected graph in O(V+E) using modified DFS.

27. **2-SAT**: Solve 2-SAT using SCC algorithm. Prove correctness.

28. **DAG Longest Path**: Find longest path in DAG using topological sort.

29. **Mother Vertex**: Find a mother vertex (can reach all others) if exists, in O(V+E).

30. **Graph Coloring**: Determine if graph is 3-colorable using BFS (decision problem).

---

## 🔥 30 Additional Advanced Problems

### Advanced Sorting & Selection (31-38)

31. **Deterministic Selection**: Implement median-of-medians with groups of 7. Why not groups of 3?

32. **X+Y Sorting**: Given sorted arrays X and Y, sort all pairs {x+y}. Beat O(n² log n).

33. **Partial Sorting**: Find k smallest elements in sorted order in O(n + k log k).

34. **Parallel Mergesort**: Design PRAM algorithm for mergesort. Analyze work and depth.

35. **In-place Mergesort**: Implement stable in-place mergesort with O(n log n) time.

36. **Adaptive Sorting**: Design algorithm that runs in O(n log(n/S)) where S is longest sorted subsequence.

37. **Integer Sorting**: Sort n integers in range [0, n²] in O(n) time.

38. **External Sorting**: Sort file too large for memory using B-way merge. Optimize I/O.

### Advanced Recurrences (39-45)

39. **Full History**: T(n) = Σ(i=1 to n-1) T(i) + n

40. **Harmonic Recurrence**: T(n) = n + (2/n)Σ(i=1 to n-1) T(i)

41. **Fractional**: T(n) = T(n^(1/2)) + 1

42. **Alternating**: T(n) = T(√n) + T(n/2) + n

43. **Probabilistic**: T(n) = T(random(1,n-1)) + n expected time

44. **Multivariate**: T(m,n) = T(m-1,n) + T(m,n-1) + 1

45. **Non-uniform**: T(n) = max{T(i) + T(n-i) + n} for i=1 to n-1

### Advanced Randomization (46-52)

46. **Karger-Stein**: Improve Karger's min-cut to O(n² log n) expected time.

47. **Hashing Analysis**: Analyze universal hashing with chaining, expected chain length.

48. **Randomized Incremental**: Build Delaunay triangulation, analyze backward analysis.

49. **Random Walk**: Cover time of random walk on n-vertex graph.

50. **Concentration Inequalities**: Apply Chernoff bounds to randomized algorithms.

51. **Las Vegas to Monte Carlo**: Convert Las Vegas algorithm to Monte Carlo with error bound.

52. **Bloom Filters**: Analyze false positive probability with k hash functions.

### Advanced Graphs (53-60)

53. **K-Core Decomposition**: Find k-core in O(V+E) time.

54. **Articulation Points**: Find all articulation points using single DFS.

55. **Eulerian Path**: Find Eulerian path if exists in O(E) time.

56. **Tournament SCC**: Every tournament has Hamiltonian path. Prove using SCC.

57. **Transitive Closure**: Compute using matrix multiplication vs. DFS trade-offs.

58. **Graph Isomorphism**: Design algorithm for trees in O(n log n).

59. **Planarity Testing**: Check if graph is planar in O(V) time (approach only).

60. **Dynamic Connectivity**: Support edge insertions and connectivity queries.

---

## 📖 Deep Understanding Guidelines

### For Each Algorithm, Master:

1. **Correctness Proof**
   - Loop invariants
   - Induction
   - Contradiction/Contrapositive

2. **Complexity Analysis**
   - Best, worst, average cases
   - Space complexity
   - Cache performance

3. **Implementation Details**
   - Edge cases
   - Optimization tricks
   - Common bugs

4. **Variations & Extensions**
   - Different input assumptions
   - Parallel versions
   - Online/streaming variants

5. **Lower Bounds**
   - Information-theoretic
   - Adversary arguments
   - Reduction proofs

---

## 💡 Problem-Solving Strategy

### When You See a Problem:

1. **Classify It**
   - What algorithm paradigm applies?
   - Similar to known problem?

2. **Start Simple**
   - Brute force first
   - Small examples by hand
   - Identify patterns

3. **Optimize Systematically**
   - Remove redundant work
   - Apply appropriate data structures
   - Consider randomization

4. **Prove Correctness**
   - State invariants clearly
   - Handle all cases
   - Check termination

5. **Analyze Completely**
   - Tight bounds
   - All complexity measures
   - Expected vs. worst case

---

## 🎓 Exam Day Strategy

### Time Management (90 minutes typical):
- **5 min**: Read all problems
- **10 min**: Quick easy problems
- **60 min**: Core problems (20 min each)
- **10 min**: Review and edge cases
- **5 min**: Buffer for surprises

### Problem Approach:
1. **State assumptions clearly**
2. **Write pseudocode before coding**
3. **Show your work for partial credit**
4. **Verify with small examples**
5. **State complexity explicitly**

### Common Pitfalls to Avoid:
- Off-by-one errors in loops
- Forgetting base cases in recursion
- Incorrect recurrence formulation
- Missing edge cases (empty input, single element)
- Not handling disconnected graphs
- Integer overflow in computations

---

## 📊 Quick Reference Complexity Table

| Algorithm | Best | Average | Worst | Space | Stable? |
|-----------|------|---------|-------|-------|---------|
| Insertion Sort | O(n) | O(n²) | O(n²) | O(1) | Yes |
| Merge Sort | O(n log n) | O(n log n) | O(n log n) | O(n) | Yes |
| Quick Sort | O(n log n) | O(n log n) | O(n²) | O(log n) | No |
| Randomized QS | O(n log n) | O(n log n) | O(n²) | O(log n) | No |
| BFS | O(V+E) | O(V+E) | O(V+E) | O(V) | - |
| DFS | O(V+E) | O(V+E) | O(V+E) | O(V) | - |
| Topological Sort | O(V+E) | O(V+E) | O(V+E) | O(V) | - |
| SCC (Kosaraju) | O(V+E) | O(V+E) | O(V+E) | O(V) | - |

---

## 🔗 Additional Study Resources

### Video Lectures
- [MIT 6.006 Fall 2011 - Srini Devadas & Erik Demaine](https://www.youtube.com/playlist?list=PLUl4u3cNGP61Oq3tWYp6V_F-5jb5L2iHb)
- [Stanford Algorithms - Tim Roughgarden](https://www.youtube.com/playlist?list=PLXFMmlk03Dt7Q0xr1PIAriY5623cKiH7V)
- [Princeton Algorithms - Robert Sedgewick](https://www.coursera.org/learn/algorithms-part1)

### Practice Platforms
- [CSES Problem Set - Sorting and Searching](https://cses.fi/problemset/)
- [LeetCode Sorting Problems](https://leetcode.com/tag/sorting/)
- [HackerRank Algorithm Practice](https://www.hackerrank.com/domains/algorithms)

### Visualization Tools
- [VisuAlgo](https://visualgo.net/)
- [Algorithm Visualizer](https://algorithm-visualizer.org/)
- [USFCA Visualization](https://www.cs.usfca.edu/~galles/visualization/Algorithms.html)

### Advanced Textbooks
- Kleinberg & Tardos: Algorithm Design
- Dasgupta, Papadimitriou, Vazirani: Algorithms
- Sedgewick & Wayne: Algorithms (4th Edition)

---

## ⚡ Quick Formulas & Identities

### Summations
- Arithmetic: Σ(i=1 to n) i = n(n+1)/2
- Geometric: Σ(i=0 to n) r^i = (r^(n+1) - 1)/(r-1)
- Harmonic: H_n = Σ(i=1 to n) 1/i ≈ ln(n) + γ

### Logarithms
- log(ab) = log(a) + log(b)
- log(a^n) = n·log(a)
- log_a(n) = log(n)/log(a)
- log(n!) ≈ n·log(n) - n (Stirling)

### Probability
- P(A∪B) = P(A) + P(B) - P(A∩B)
- E[X+Y] = E[X] + E[Y] (always!)
- Var(X) = E[X²] - (E[X])²

### Master Theorem Boundary
- n^(log_b(a)) dominates? → Case 1
- Equal with log factors? → Case 2  
- f(n) dominates polynomially? → Case 3

---

## 🏆 Final Preparation Checklist

### 3 Days Before:
- [ ] Review all algorithms' pseudocode
- [ ] Solve 5 new medium problems
- [ ] Make formula sheet

### 1 Day Before:
- [ ] Quick review of complexity proofs
- [ ] Practice 3 hard problems timed
- [ ] Review common mistakes list

### Exam Day:
- [ ] Bring: pencils, eraser, calculator (if allowed)
- [ ] Review quick reference sheet
- [ ] Stay calm, you're prepared!

---

*Remember: Understanding > Memorization. Focus on the "why" behind each algorithm!*