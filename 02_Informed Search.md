# Informed Search

[31 Jan](https://www.notion.so/31-Jan-18c28e7162a58019b71bd3e6cac961f5?pvs=21) 

## 🗂️ **Summary of Key Concepts**

| **Concept** | **Description** | ⚡**Key Points** | ⚠️**Common Pitfalls** |
| --- | --- | --- | --- |
| **Uninformed Search** | Uses only problem formulation details (e.g., path-cost) | No domain-specific knowledge, explores broadly | Inefficient for large search spaces |
| **Informed Search** | Uses heuristics (启发式函数) to guide the search | More efficient, focuses on promising paths | Poor heuristics can reduce performance |
| **Heuristic (h(n))** | Estimate of cost from node *n* to goal | Must be admissible (不高估成本) for optimality | Overestimating leads to suboptimal paths |
| **Greedy Best-First Search** | Expands node with the lowest heuristic cost | Fast but not always optimal | Ignores actual path-cost, may miss optimal solution |
| *A* Search* | Considers both path-cost and heuristic: f(n) = g(n) + h(n) | Optimal with admissible and consistent heuristics | Memory-intensive in large graphs |
| **Admissible Heuristic** | Never overestimates cost to the goal | Guarantees optimal solutions in A* search | May be less informed, causing more node expansions |
| **Consistent Heuristic** | Heuristic satisfies h(n) ≤ cost(n, n') + h(n') | Ensures non-decreasing f(n) values along paths | Not all admissible heuristics are consistent |
| **Dominant Heuristic** | One heuristic consistently better than another | Use max of multiple admissible heuristics for dominance | Combining poor heuristics doesn't improve performance |
| *Weighted A* Search* | Uses f(n) = g(n) + w × h(n) where w > 1 | Faster with bounded sub-optimality | Violates optimality if w is too large |
| **Beam Search** | Keeps only top *k* nodes in frontier | Memory-efficient variant of best-first search | Can miss optimal paths due to aggressive pruning |

---

## 🔍 **1. Informed vs. Uninformed Search**

- **Uninformed Search:** Uses only problem structure (e.g., BFS, DFS, UCS).
- **Informed Search:** Uses domain-specific information (heuristics) to improve efficiency.

**Key Difference:**

Informed search algorithms are more efficient because they prioritize nodes likely to lead to the goal.

---

## 💡 **2. Heuristic Functions**

- **Definition:** A heuristic function h(n) estimates the cost from node n to the goal.
- **Example:** In the 8-puzzle, h(n) could be the number of misplaced tiles.

h(n) = Number of misplaced tiles

### ✅ **Admissible Heuristic**

- Never overestimates the actual cost.
- Example: Straight-line distance (SLD) in route planning.

### ✅ **Consistent Heuristic**

- For all nodes n and successors n':

h(n) ≤ cost(n, n') + h(n')

- Ensures that once a node is expanded, the shortest path to it is found.

---

## 🚀 **3. Greedy Best-First Search**

- **Strategy:** Always expands the node with the lowest heuristic cost h(n).
- **Evaluation Function:**

f(n) = h(n)

- **Advantage:** Fast for simple heuristics.
- **Drawback:** Not optimal; ignores actual path-cost (g(n)).

---

## ⭐ *4. A* Search Algorithm*

- **Evaluation Function:**

f(n) = g(n) + h(n)

Where:

- g(n) = cost from the start node to n
- h(n) = estimated cost from n to the goal

**Key Properties:**

- **Optimality:** Guaranteed if h(n) is admissible.
- **Efficiency:** Expands fewer nodes than uninformed search.

### Example:

f(n) = Actual path cost + Estimated cost to goal

---

## 🎯 **5. Heuristic Quality: Admissibility & Consistency**

- **Admissibility:** h(n) never overestimates the true cost.
- **Consistency (Monotonicity):** f(n) values are non-decreasing along a path.

**Relationship:**

Consistency → Admissibility
Admissibility ↛ Consistency

---

## 🚩 **6. Advanced Heuristic Strategies**

### 🌍 **Dominant Heuristics**

- If h₁(n) ≥ h₂(n) for all n, then h₁ dominates h₂.
- Use the **maximum** of multiple heuristics:

h(n) = max(h₁(n), h₂(n), ..., hₖ(n))

### 📉 *Weighted A* Search*

- Adjusts A* with a weight factor w:

f(n) = g(n) + w × h(n) (w > 1)

- Faster, but may lose optimality.

### 📊 **Beam Search**

- Keeps only the top k nodes in the frontier.
- Reduces memory usage but risks missing the optimal solution.

---

## 📏 **7. Measuring Search Efficiency**

- **Effective Branching Factor (b*):**Measures how effectively the algorithm prunes the search space.
- **Search Contours:**Visualize nodes expanded based on f(n) values.

---

## 🧩 **8. Deriving Admissible Heuristics**

1. **Relaxed Problems:** Simplify constraints to find easier solutions.
2. **Subproblems:** Use pattern databases to precompute solutions.
3. **Landmark-Based Heuristics:** Use key points (anchors) to estimate distances.

---

## 🔑 **9. Key Takeaways**

- Informed search is more efficient than uninformed search.
- A* search is optimal with admissible and consistent heuristics.
- Greedy search is faster but not always optimal.
- Heuristics significantly affect search performance.

---

# 🎯 **Formulas to Remember**

1. *A* Evaluation Function:*f(n) = g(n) + h(n)
2. **Greedy Best-First Search:**f(n) = h(n)
3. *Weighted A* Search:*f(n) = g(n) + w × h(n)
4. **Consistency Condition:**h(n) ≤ cost(n, n') + h(n')
5. **Dominant Heuristic:**h(n) = max(h₁(n), h₂(n), ..., hₖ(n))

---

**Happy Learning! 🚀**