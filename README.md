# 🔥 DSA Pattern Recognition Master Repository

> **Identify Pattern → Choose Data Structure → Predict Complexity → Solve**

---

🚀 **A Senior-Level, Interview-Ready Guide to Data Structures & Algorithms**  
Designed with **Top Egnineering Knowledge from Books rigor**, this repository focuses on **pattern recognition, trade-offs, invariants, and complexity analysis** — not rote memorization.

---

## 🔗 Learn With Me

[![YouTube](https://img.shields.io/badge/YouTube-red?style=for-the-badge&logo=youtube&logoColor=white)](https://www.youtube.com/@freebirdscrew2023)
[![Medium](https://img.shields.io/badge/Medium-black?style=for-the-badge&logo=medium&logoColor=white)](https://medium.com/@simranjeetsingh1497)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-blue?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/simranjeet97/)

---

## 🧠 What This Repository Teaches

- 🔍 How to **identify the correct DSA pattern** just by reading the problem  
- 🧩 How to **choose the right data structure** based on constraints  
- ⚖️ How to **defend your approach** using alternatives & trade-offs  
- ⏱️ How to **predict time & space complexity before coding**  
- 🗣️ How to **communicate solutions like a Senior / Staff Engineer**

---

## 🗺️ Covered Topics

`Sliding Window` • `Two Pointers` • `Prefix Sum` • `Binary Search` • `Dynamic Programming`  
`Greedy` • `Backtracking` • `Stacks & Queues` • `Trees` • `Graphs` • `Union-Find`  
`Heaps` • `Tries` • `Composite Patterns` • `MNC-Style Interview Reasoning`

---

## 🎯 Who This Is For

- ✅ Engineers preparing for **FAANG / Big Tech interviews**
- ✅ Developers targeting **L5 (Senior) and above**
- ✅ Anyone who wants to **think in patterns instead of memorizing solutions**

---

## 🧪 How to Use This Repository

1. Read the **pattern recognition signals**
2. Study **alternatives & trade-offs**
3. Understand **why other approaches fail**
4. Apply the reasoning to **real interview problems**

---

⭐ **If this repository helps you think better, consider starring it.**  
This is built to make you **dangerous in technical interviews**.


## 0️⃣ TOP SOFTWARE ENGINEER OR MACHINE LEARNING ENGINEER MINDSET (READ THIS FIRST)

You are evaluated on:
- Correctness (proof, not intuition)
- Trade-offs (why this, not that)
- Edge cases & failure modes
- Ability to combine patterns
- Clear communication

> ❗ Patterns are assumed. **Judgment is tested.**

---

## 0️⃣ HOW TO READ ANY DSA QUESTION (UNIVERSAL FRAMEWORK)

### Step 1: Identify Input Type

| Input Type | Immediately Think |
|----------|------------------|
| Array / String | Sliding Window, Two Pointers, Prefix Sum, Binary Search |
| Linked List | Fast & Slow Pointers, Reversal |
| Stack | Monotonic Stack, Expression Parsing |
| Queue | BFS, Level Order |
| Tree | DFS, BFS, Recursion |
| Graph | BFS, DFS, Topological Sort, Union-Find |
| Matrix / Grid | BFS, DFS, DP |
| Stream / Online | Heap |
| Dictionary / Prefix | Trie |

---

### Step 2: Keywords → Pattern Mapping

| Keyword in Problem | Pattern |
|------------------|--------|
| contiguous subarray / substring | Sliding Window |
| longest / shortest / max / min | Sliding Window / DP / Greedy |
| sorted | Binary Search / Two Pointers |
| pair / triplet | Two Pointers |
| prefix / suffix | Prefix Sum / Trie |
| all combinations | Backtracking |
| optimal / maximum / minimum | DP or Greedy |
| dependency / prerequisite | Topological Sort |
| connected / reachable | BFS / DFS |
| cycle | DFS / Union-Find |
| k largest / smallest | Heap |

---

### Step 3: Constraints → Complexity Filter

| Input Size (N) | Expected Complexity |
|--------------|--------------------|
| N ≤ 100 | O(N²), O(N³) |
| N ≤ 10⁴ | O(N²) borderline |
| N ≤ 10⁵ | O(N log N) |
| N ≤ 10⁶ | O(N) |
| Subsets / permutations | Exponential |

---

### Step 4: Question Intent

- Decision (Yes / No)
- Count number of ways
- Optimization (Max / Min)
- Generate all answers

---

## 1️⃣ ARRAY & STRING PATTERNS

---

## 🟦 Sliding Window

### When to Use
- Contiguous subarray or substring
- Fixed or variable size
- Large constraints

### Types
- Fixed Window
- Variable Window

### Example (Fixed Window)
**Problem:** Maximum sum of subarray of size `K`

**Pattern Recognition:**
- Subarray
- Fixed size
- Contiguous

**Complexity:**
- Time: O(N)
- Space: O(1)

---

### Example (Variable Window)
**Problem:** Longest substring without repeating characters

**Pattern:**
- Sliding Window + HashSet

**Complexity:**
- Time: O(N)
- Space: O(Alphabet)

---

### Sliding Window Checklist
- Can I expand right pointer?
- Can I shrink left pointer?
- Can I update result incrementally?

### Failure Cases
- ❌ Non-contiguous data
- ❌ Negative numbers (for sum-based windows)
- ❌ When shrinking condition is unclear

### Invariant
> The window always represents a **valid contiguous segment**,  
> and each element **enters and leaves at most once**.

### Alternatives & Trade-offs (With Reasoning)

| Approach | Time | Space | Why / Why Not |
|--------|------|-------|---------------|
| Brute Force | O(N²) | O(1) | Recomputes the same subarray sums repeatedly |
| Sliding Window | O(N) | O(1) | Optimal when window updates are incremental |
| Prefix Sum | O(N) | O(N) | Extra memory, unnecessary if window is adjustable |
| DP | O(N) | O(N) | Overkill, no overlapping subproblems |

#### Why Others Are Not Ideal
- **Brute Force** recalculates sums for overlapping subarrays → violates efficiency for large N  
  _Example_: Max subarray of size K recalculates K elements each time.
- **Prefix Sum** stores cumulative sums, but sliding window already maintains the sum in O(1).
- **DP** is meant for overlapping subproblems; sliding window problems are linear scans.

#### When Alternatives Are Better
- Use **Prefix Sum** when:
  - Negative numbers exist
  - Window size is not controllable
- Use **DP** when:
  - State depends on previous optimal results (e.g., Kadane’s)

---

## 🟦 Two Pointers

### When to Use
- Sorted arrays
- Pair / triplet problems
- In-place modification

### Example
**Problem:** Two Sum (sorted array)

### Invariant
> Left pointer only moves forward,  
> right pointer only moves backward —  
> guaranteeing no repeated work.

### Failure Cases
- ❌ Unsorted array (unless sorted first)
- ❌ Requires index preservation (sorting breaks it)

**Pattern:** Two Pointers

**Complexity:**
- Time: O(N)
- Space: O(1)

---

### Variants

| Problem | Technique |
|------|-----------|
| Remove duplicates | Slow & Fast pointers |
| 3Sum | Fix one + two pointers |
| Container with most water | Two ends |

### Alternatives & Trade-offs (With Reasoning)

| Approach | Time | Space | Why / Why Not |
|--------|------|-------|---------------|
| Brute Force | O(N²) | O(1) | Checks all pairs redundantly |
| Two Pointers | O(N) | O(1) | Exploits sorted property |
| Hashing | O(N) | O(N) | Uses extra memory |
| Binary Search | O(N log N) | O(1) | Slower than linear scan |

#### Why Others Are Not Ideal
- **Hashing** ignores sorted order and trades space for time.
- **Binary Search** works per element, but total becomes N log N.
- **Brute Force** doesn’t leverage ordering at all.

#### When Alternatives Are Better
- Use **Hashing** when:
  - Array is unsorted
  - Index preservation matters
- Use **Binary Search** when:
  - One side is fixed, and search space is independent

---

## 🟦 Prefix Sum

### When to Use
- Range queries
- Subarray sum problems
- Repeated sum calculations

### Invariant
> `prefix[j] - prefix[i]` gives sum of subarray `(i, j]`.

### Example
**Problem:** Subarray sum equals K

**Pattern:** Prefix Sum + HashMap

**Complexity:**
- Time: O(N)
- Space: O(N)

### Why Sliding Window Fails Here
- Negative numbers break monotonicity

### Alternatives & Trade-offs (With Reasoning)

| Approach | Time | Space | Why / Why Not |
|--------|------|-------|---------------|
| Brute Force | O(N²) | O(1) | Recalculates sums |
| Sliding Window | O(N) | O(1) | Fails with negative numbers |
| Prefix Sum | O(N) | O(N) | Handles negatives robustly |
| Segment Tree | O(N log N) | O(N) | Too heavy without updates |

#### Why Others Are Not Ideal
- **Sliding Window** assumes monotonic behavior; negatives break it.
  _Example_: Subarray sum = K with negative values.
- **Segment Tree** is meant for frequent updates, not static queries.

#### When Alternatives Are Better
- Use **Segment Tree** when:
  - Updates + queries are both required
- Use **Sliding Window** when:
  - All values are positive

---

## 2️⃣ LINKED LIST PATTERNS

---

## 🟦 Fast & Slow Pointers

### When to Use
- Cycle detection
- Find middle
- Palindrome check

### Invariant
> Fast pointer moves twice as fast →  
> collision implies a cycle.

### Example
**Problem:** Detect cycle in linked list

**Complexity:**
- Time: O(N)
- Space: O(1)

### Alternatives & Trade-offs (With Reasoning)

| Approach | Time | Space | Why / Why Not |
|--------|------|-------|---------------|
| Hash Set | O(N) | O(N) | Extra memory |
| Fast & Slow | O(N) | O(1) | Memory optimal |

#### Why Others Are Not Ideal
- **Hash Set** stores visited nodes, violating space efficiency.
- Fast/slow leverages pointer movement behavior inherently.

#### When Alternatives Are Better
- Use **Hash Set** when:
  - Simpler implementation is preferred
  - Memory is not a concern

---

## 🟦 Linked List Reversal

### Problems
- Reverse linked list
- Reverse in K-group

### Alternatives & Trade-offs (With Reasoning)

| Approach | Time | Space | Why / Why Not |
|--------|------|-------|---------------|
| Iterative | O(N) | O(1) | Preferred, memory efficient |
| Recursive | O(N) | O(N) | Clean but stack usage |
| Stack-based | O(N) | O(N) | Unnecessary extra space |

#### Why Others Are Not Ideal
- **Recursive approach** uses the call stack to store function frames, which grows linearly with list size.  
  _Example_: Reversing a list of 10⁶ nodes risks stack overflow.
- **Stack-based approach** stores all nodes explicitly, duplicating what pointers already provide.

#### When Alternatives Are Better
- Use **Recursive reversal** when:
  - Code clarity is prioritized
  - List size is small and controlled
- Use **Stack-based reversal** when:
  - Nodes cannot be modified directly (immutable structure)
- Use **Iterative reversal** when:
  - Memory efficiency and safety matter (production systems)

---

## 3️⃣ STACK PATTERNS

---

## 🟦 Stack

### When to Use
- Valid parentheses
- Expression evaluation
- Undo/Redo

### Example
**Problem:** Valid Parentheses

**Complexity:**
- Time: O(N)
- Space: O(N)

### Alternatives & Trade-offs (With Reasoning)

| Approach | Time | Space | Why / Why Not |
|--------|------|-------|---------------|
| Stack | O(N) | O(N) | Correct abstraction |
| Recursion | O(N) | O(N) | Risk of stack overflow |
| Regex / Parsing | ❌ | ❌ | Unsafe / unreadable |

#### Why Others Are Not Ideal
- **Recursion** implicitly uses the call stack, which is not under your control and may overflow.  
  _Example_: Evaluating deeply nested parentheses `"((((...))))"`.
- **Regex/parsing hacks** lack structural guarantees and fail on nested patterns.

#### When Alternatives Are Better
- Use **Recursion** when:
  - Depth is guaranteed small
  - Simpler conceptual model is desired
- Use **Regex** when:
  - Pattern is flat and non-nested (e.g., token validation)
- Use **Explicit Stack** when:
  - Nested or LIFO behavior is fundamental (expression evaluation)


---

## 🟦 Monotonic Stack

### When to Use
- Next greater/smaller element
- Histogram problems

### Invariant (Monotonic Stack)
> Stack maintains increasing or decreasing order  
> ensuring each element is pushed and popped once.

### Example
**Problem:** Largest Rectangle in Histogram

**Complexity:**
- Time: O(N)
- Space: O(N)
### Alternatives & Trade-offs (With Reasoning)

| Approach | Time | Space | Why / Why Not |
|--------|------|-------|---------------|
| Brute Force | O(N²) | O(1) | Nested scans |
| Monotonic Stack | O(N) | O(N) | Each element processed once |
| Segment Tree | O(N log N) | O(N) | Overkill |

#### Why Others Are Not Ideal
- **Brute Force** rechecks next elements repeatedly.
- **Segment Tree** supports range queries but doesn’t exploit order.

#### When Alternatives Are Better
- Use **Segment Tree** when:
  - Dynamic updates are needed
- Use **Brute Force** for tiny inputs

---

## 4️⃣ BINARY SEARCH PATTERNS

---

## 🟦 Binary Search on Array

### When to Use
- Sorted data
- Find index or boundary

### Invariant
> Search space always contains the answer.

### Complexity
- Time: O(log N)

### Alternatives & Trade-offs

| Approach | Time | Space | Why / Why Not |
|--------|------|-------|---------------|
| Linear Scan | O(N) | O(1) | Acceptable for small N |
| Binary Search | O(log N) | O(1) | Optimal for sorted data |
| Hashing | O(N) | O(N) | Loses ordering |

---

## 🟦 Binary Search on Answer

### When to Use
- Monotonic condition
- Minimum or maximum feasible answer

**Signal:**
- "Minimum X such that…"
- Feasibility check is monotonic

### Example
**Problem:** Minimum days to ship packages

### Composite Pattern
**Binary Search + Greedy Check**
### Example
**Minimum Days to Ship Packages**

### Alternatives & Trade-offs (With Reasoning)

| Approach | Time | Space | Why / Why Not |
|--------|------|-------|---------------|
| Brute Force | O(N×M) | O(1) | Tries all answers |
| Binary Search | O(N log M) | O(1) | Exploits monotonic feasibility |
| DP | O(N×M) | O(N) | Heavy state space |

#### Why Others Are Not Ideal
- **DP** computes all states even though only feasibility is needed.
- **Brute Force** doesn’t exploit monotonicity.

#### When Alternatives Are Better
- Use **DP** when:
  - Multiple queries on same state space
- Use **Binary Search** when:
  - Feasibility strictly monotonic

---

## 5️⃣ RECURSION & BACKTRACKING

---

## 🟦 Backtracking

### When to Use
- All combinations/permutations
- Constraint satisfaction problems

### Invariant
> Partial solution is always valid.

### Examples

| Problem | Pattern |
|------|--------|
| N-Queens | Backtracking |
| Sudoku | Backtracking |
| Subsets | Backtracking |

**Complexity:** Exponential

### Alternatives & Trade-offs (With Reasoning)

| Approach | Time | Space | Why / Why Not |
|--------|------|-------|---------------|
| Brute Force | Exponential | — | No pruning |
| Backtracking | Exponential | O(depth) | Prunes invalid paths |
| DP | ❌ | ❌ | Can't enumerate all solutions |

#### Why Others Are Not Ideal
- **Brute Force** blindly explores every possibility, even invalid ones.  
  _Example_: Generating all subsets without stopping early on invalid states.
- **DP** optimizes for optimal values, not enumeration of valid combinations.

#### When Alternatives Are Better
- Use **DP** when:
  - Only the count or optimal value is required  
  _Example_: Count of subsets with sum K
- Use **Brute Force** when:
  - Input size is extremely small
- Use **Backtracking** when:
  - Constraints allow early pruning  
  _Example_: N-Queens, Sudoku, combinations with constraints

---

## 6️⃣ DYNAMIC PROGRAMMING (DP)

---

## 🟦 When to Use DP
- Optimal substructure (min/max)
- Overlapping subproblems
- Choice-based problems (states)

---

## DP Formula
- State
- Transition
- Base Case

---

### Common DP Types

| Type | Example |
|----|--------|
| 1D DP | Fibonacci |
| 2D DP | LCS |
| Knapsack | 0/1 Knapsack |
| Grid DP | Unique Paths |
| String DP | Edit Distance |
| Tree DP | Diameter |

### Invariant
> DP state represents optimal solution up to that point.

---

### Example
**Coin Change**

- State: `dp[amount]`
- Transition: `dp[a] = min(dp[a - coin])`

### Alternatives & Trade-offs (With Reasoning)

| Approach | Time | Space | Why / Why Not |
|--------|------|-------|---------------|
| Greedy | O(N) | O(1) | Fails without greedy-choice proof |
| DP | Polynomial | Polynomial | Guarantees optimality |
| Backtracking | Exponential | Stack | Explores all possibilities |

#### Why Others Are Not Ideal
- **Greedy** fails if local optimum ≠ global optimum  
  _Example_: 0/1 Knapsack
- **Backtracking** doesn’t reuse overlapping subproblems.

#### When Alternatives Are Better
- Use **Greedy** when:
  - Greedy-choice property proven
- Use **Backtracking** when:
  - All solutions required

---

## 7️⃣ GREEDY ALGORITHMS

---

## 🟦 When to Use Greedy
- Local optimal leads to global optimal
- Sorting helps
- One-pass decisions

### Invariant
> Greedy choice does not block optimal solution.

---

### Examples

| Problem | Greedy Choice |
|------|--------------|
| Activity Selection | Earliest finish |
| Fractional Knapsack | Highest value/weight |
| Gas Station | Max reachable |

**Complexity:** O(N log N)

### Alternatives & Trade-offs

| Approach | Time | Space | Why / Why Not |
|--------|------|-------|---------------|
| DP | O(N²) | O(N²) | Correct but slower |
| Greedy | O(N log N) | O(1) | Optimal if greedy property holds |
| Backtracking | Exponential | — | Too slow |

---

## 8️⃣ TREE PATTERNS

---

## 🟦 DFS on Trees

### When to Use
- Height
- Diameter
- Path problems

### Alternatives & Trade-offs

| Approach | Time | Space | Why / Why Not |
|--------|------|-------|---------------|
| DFS (Recursive) | O(N) | O(H) | Simple |
| DFS (Iterative) | O(N) | O(H) | Avoid recursion |
| BFS | O(N) | O(N) | Uses more memory |

---

## 🟦 BFS on Trees

### When to Use
- Level order traversal
- Shortest path
- Zigzag traversal

### Alternatives & Trade-offs

| Approach | Time | Space | Why / Why Not |
|--------|------|-------|---------------|
| BFS | O(N) | O(N) | Best for level order |
| DFS | O(N) | O(H) | Harder to manage levels |

---

## 9️⃣ GRAPH PATTERNS

---

## 🟦 BFS

### When to Use
- Shortest path (unweighted)
- Grid problems

### Alternatives & Trade-offs (With Reasoning)

| Approach | Time | Space | Why / Why Not |
|--------|------|-------|---------------|
| DFS | O(V+E) | O(V) | No shortest path |
| BFS | O(V+E) | O(V) | Shortest path guaranteed |
| Dijkstra | O(E log V) | O(V) | Overkill for unweighted |

#### Why Others Are Not Ideal
- **DFS** explores depth-first, not level-first.
- **Dijkstra** adds unnecessary heap overhead.

#### When Alternatives Are Better
- Use **DFS** for cycle detection
- Use **Dijkstra** for weighted graphs

---

## 🟦 DFS

### When to Use
- Cycle detection
- Connected components

### Alternatives & Trade-offs

| Approach | Time | Space | Why / Why Not |
|--------|------|-------|---------------|
| DFS | O(V+E) | O(V) | Cycle detection |
| BFS | O(V+E) | O(V) | Less natural for cycles |
| Union-Find | O(E α(V)) | O(V) | No traversal info |

---

## 🟦 Topological Sort

### When to Use
- Dependency ordering
- DAG problems

### Alternatives & Trade-offs

| Approach | Time | Space | Why / Why Not |
|--------|------|-------|---------------|
| DFS-based | O(V+E) | O(V) | Simple |
| Kahn’s (BFS) | O(V+E) | O(V) | Better cycle detection |
| DP | ❌ | ❌ | Not applicable |

---

## 🟦 Union-Find

### When to Use
- Connectivity
- Cycle detection in undirected graph
  
### Alternatives & Trade-offs (With Reasoning)

| Approach | Time | Space | Why / Why Not |
|--------|------|-------|---------------|
| DFS/BFS | O(V+E) | O(V) | Static connectivity |
| Union-Find | O(E α(V)) | O(V) | Dynamic connectivity |

#### Why Others Are Not Ideal
- DFS/BFS recompute connectivity every time.
- Union-Find maintains connectivity incrementally.

#### When Alternatives Are Better
- Use **DFS/BFS** when:
  - Single static traversal needed


---

## 🔟 HEAP / PRIORITY QUEUE

---

## 🟦 When to Use Heap
- K largest / smallest
- Streaming data
- Dijkstra / Prim

### Invariant
> Heap root always holds highest/lowest priority element.

### Alternatives & Trade-offs (With Reasoning)

| Approach | Time | Space | Why / Why Not |
|--------|------|-------|---------------|
| Sorting | O(N log N) | O(1) | Full order unnecessary |
| Heap | O(N log K) | O(K) | Maintains partial order |
| QuickSelect | O(N) avg | O(1) | Worst-case risk |

#### Why Others Are Not Ideal
- **Sorting** solves more than required.
- **QuickSelect** is unstable in worst-case.

#### When Alternatives Are Better
- Use **Sorting** when:
  - Full order required
- Use **QuickSelect** when:
  - One-time selection and average case acceptable

---

### Example
**Problem:** Kth largest element

**Pattern:** Min Heap of size K

---

## 1️⃣1️⃣ TRIE

---

## 🟦 When to Use Trie
- Prefix search
- Autocomplete
- Dictionary problems

### Alternatives & Trade-offs (With Reasoning)

| Approach | Time | Space | Why / Why Not |
|--------|------|-------|---------------|
| Brute String Match | O(N×M) | O(1) | Repeated scans |
| HashMap | O(1) | O(N×M) | No prefix logic |
| Trie | O(M) | O(total chars) | Prefix-optimized |

#### Why Others Are Not Ideal
- **HashMap** can’t answer prefix queries efficiently.
- **Brute Force** compares every string fully.

#### When Alternatives Are Better
- Use **HashMap** when:
  - Exact match only
- Use **Trie** when:
  - Prefix search required

---

## 1️⃣5️⃣ COMPOSITE PATTERNS (CRITICAL)

| Combination | Example |
|----------|--------|
| Binary Search + Greedy | Ship packages |
| BFS + State | Shortest path with keys |
| DFS + DP | Tree DP |
| Trie + DFS | Word Search II |
| Heap + Sliding Window | Sliding window median |
| Union-Find + Sorting | Kruskal MST |
| DP + Bitmask | TSP |

---

## 🧠 FINAL INTERVIEW MANTRA

> “I chose **[pattern]** because **[signal]**,  
> the invariant is **[truth]**,  
> complexity is **[T/S]**,  
> edge cases are **[cases]**,  
> alternatives were **[trade-offs]**.”

---

## ✅ HOW TO PRACTICE
1. Solve by **pattern**, not random problems
2. Say the pattern out loud before coding
3. Write complexity before code
4. Re-solve after 7 days

---

🔥 **Master this document and DSA becomes pattern recognition, not guesswork.**
