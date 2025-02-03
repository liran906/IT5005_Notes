# Uninformed Search (无信息搜索)

## 🔹 Definition

Uninformed search refers to a category of search algorithms that explore the state space **without any prior knowledge** about the goal's location or the best path to reach it. These algorithms rely solely on the structure of the problem, rather than using **heuristic information** to guide the search.

---

## 🔹 Types of Uninformed Search

Uninformed search algorithms can be categorized based on two criteria:

### 1️⃣ **Based on Storage of Nodes**

- **Graph Search** (图搜索)
    - Stores reached nodes to **avoid cycles** and redundant paths.
    - Useful when the search space contains loops or revisits states.
- **Tree Search** (树搜索)
    - Does not store reached nodes, meaning it can **revisit the same state multiple times**.
    - Suitable for problems where re-exploration is acceptable.

### 2️⃣ **Based on Traversal Strategy**

- **Breadth-First Search (BFS, 广度优先搜索)**
- **Depth-First Search (DFS, 深度优先搜索)**
- **Depth-Limited Search (DLS, 深度限制搜索)**
- **Iterative Deepening Search (IDDFS, 迭代加深搜索)**
- **Bidirectional Search (双向搜索)**
- **Uniform Cost Search (UCS, 统一代价搜索)**

---

## 🔹 Graph Search vs. Tree Search

| Feature | **Graph Search (图搜索)** | **Tree Search (树搜索)** |
| --- | --- | --- |
| **Stores reached nodes?** | ✅ Yes | ❌ No |
| **Handles cycles?** | ✅ Prevents infinite loops | ❌ May revisit states |
| **Memory usage** | 🟡 Higher (stores visited nodes) | 🟢 Lower (no extra storage) |
| **Time efficiency** | 🟢 More efficient (avoids redundant paths) | 🟡 May re-explore paths |
| **Use case** | When the search space has cycles or repeated states | When repeated exploration is acceptable |

### 📝 **Why Store Reached Nodes?**

- If the search space **contains cycles or redundant paths**, storing visited nodes helps prune the search tree and improve efficiency.
- Graph search is particularly useful in **pathfinding problems** (e.g., navigating a road network), while tree search is commonly used when every decision leads to a unique new state.

---

## 🔹 Common Uninformed Search Algorithms

| Algorithm | Description | Time Complexity |
| --- | --- | --- |
| **Breadth-First Search (BFS, 广度优先搜索)** | Explores nodes level by level, ensuring the shortest path in an unweighted graph | O(b^d) |
| **Depth-First Search (DFS, 深度优先搜索)** | Explores one branch deeply before backtracking | O(b^d) |
| **Uniform Cost Search (UCS, 统一代价搜索)** | Expands the node with the lowest path cost | O(b^d) |
| **Depth-Limited Search (DLS, 深度限制搜索)** | DFS with a depth limit to avoid infinite loops | O(b^d) |
| **Iterative Deepening DFS (IDS, 迭代加深深度优先搜索)** | Runs DFS with increasing depth limits, combining benefits of BFS and DFS | O(b^d) |

where:

b (branching factor, number of children per node)
d (depth of the shallowest goal node)

---

## 🔹 Comparison: Uninformed vs. Informed Search

|  | **Uninformed Search** | **Informed Search** |
| --- | --- | --- |
| Uses additional knowledge? | ❌ No | ✅ Yes (heuristics) |
| Examples | BFS, DFS, UCS, IDDFS | A\*, Greedy Best-First Search |
| Efficiency | May explore irrelevant paths | More efficient, reduces search space |
| Suitable when | No heuristic information available | Heuristic guidance is available |

### 🔹 Example Scenarios:

- **Maze solving**: BFS guarantees the shortest path, but A\* search is faster if heuristic information is available.
- **Sudoku solving**: DFS can brute-force the solution, but backtracking with heuristics is more efficient.

Uninformed search is like **blindly exploring** all possible options, while informed search is like **navigating with a map and a sense of direction**.

[Space Performance](Uninformed%20Search%20(%E6%97%A0%E4%BF%A1%E6%81%AF%E6%90%9C%E7%B4%A2)%2018c28e7162a5804aafc5e9592c76f538/Space%20Performance%2018c28e7162a5802fa47ce51bd102b66d.md)