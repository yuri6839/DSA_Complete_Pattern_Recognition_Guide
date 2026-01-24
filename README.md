# 🔥 DSA PATTERN RECOGNITION MASTER REPOSITORY
## Identify Pattern → Choose Data Structure → Predict Complexity → Solve

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

### Alternatives & Trade-offs

| Approach | Time | Space | Why / Why Not |
|-------|------|------|---------------|
| Brute Force | O(N²) | O(1) | Too slow |
| Sliding Window | O(N) | O(1) | Best |
| Prefix Sum | O(N) | O(N) | Overkill |

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

---

## 🟦 Linked List Reversal

### Problems
- Reverse linked list
- Reverse in K-group

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

---

## 8️⃣ TREE PATTERNS

---

## 🟦 DFS on Trees

### When to Use
- Height
- Diameter
- Path problems

---

## 🟦 BFS on Trees

### When to Use
- Level order traversal
- Shortest path
- Zigzag traversal

---

## 9️⃣ GRAPH PATTERNS

---

## 🟦 BFS

### When to Use
- Shortest path (unweighted)
- Grid problems

---

## 🟦 DFS

### When to Use
- Cycle detection
- Connected components

---

## 🟦 Topological Sort

### When to Use
- Dependency ordering
- DAG problems

---

## 🟦 Union-Find

### When to Use
- Connectivity
- Cycle detection in undirected graph

---

## 🔟 HEAP / PRIORITY QUEUE

---

## 🟦 When to Use Heap
- K largest / smallest
- Streaming data
- Dijkstra / Prim

### Invariant
> Heap root always holds highest/lowest priority element.

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
