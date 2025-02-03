# Space Performance

# Space Performance Comparison: BFS vs. DFS vs. IDS

## 🔹 Space Complexity Overview

| Algorithm | Space Complexity | Reason |
| --- | --- | --- |
| **Breadth-First Search (BFS, 广度优先搜索)** | O(b^d) | Stores all nodes at the current depth level |
| **Depth-First Search (DFS, 深度优先搜索)** | O(d) | Only stores nodes along the current path |
| **Iterative Deepening Search (IDS, 迭代加深搜索)** | O(d) | Similar to DFS; only keeps a single path |

where:

- b = branching factor (number of children per node)
- d = depth of the shallowest goal node

---

## 🔹 Why is DFS More Space-Efficient than BFS?

1. **DFS only stores the path from the root to the current node**, leading to O(d) space.
2. **BFS must store all nodes at the current level**, leading to O(b^d) space, which grows exponentially.
3. **IDS has the same space efficiency as DFS**, but it **recomputes nodes** to achieve completeness.

---

## 🔹 When to Use Each Algorithm?

| Scenario | Best Choice | Reason |
| --- | --- | --- |
| **Need the shortest path in an unweighted graph?** | ✅ BFS | Guarantees shortest path but uses more space |
| **Memory is limited, and depth is unknown?** | ✅ IDS | Saves space while ensuring completeness |
| **Memory is limited, and depth is fixed?** | ✅ DFS | Most space-efficient, but may not find the shortest path |

---

## 🔹 Final Takeaways

✔️ **DFS is much more space-efficient than BFS**.

✔️ **IDS has the same space efficiency as DFS but guarantees completeness like BFS**.

✔️ **Use DFS when space is a concern, but not when the shortest path is needed**.