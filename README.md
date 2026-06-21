# Greedy Best-First Search for Route Planning on the California Road Network

A Python implementation of the **Greedy Best-First Search (GBFS)** algorithm for route planning on a large-scale real-world road network dataset from the Stanford Network Analysis Project (SNAP).

## 📌 Overview

This project demonstrates the application of the **Greedy Best-First Search** algorithm to solve a route-finding problem on the **California Road Network (roadNet-CA)** dataset.

The algorithm utilizes a heuristic function to guide the search process toward the target node, aiming to reduce exploration time compared to uninformed search methods.

This project was developed as part of the **Algorithm Design and Analysis** course at the **Institut Teknologi Sumatera (ITERA)**.

---

## 🎯 Objectives

- Implement the Greedy Best-First Search algorithm in Python.
- Apply the algorithm to a large-scale real-world graph dataset.
- Analyze the algorithm's performance in terms of execution time and node expansion.
- Evaluate the impact of heuristic quality on search efficiency.

---

## 📊 Dataset

### California Road Network (roadNet-CA)

The dataset is provided by the Stanford Network Analysis Project (SNAP) and represents the road network of California, USA.

| Property | Value |
|-----------|-----------|
| Nodes | 1,965,206 |
| Edges | 5,533,214 |
| Type | Undirected Graph |
| Format | Text File (.txt) |

Dataset Source:

https://snap.stanford.edu/data/roadNet-CA.html

---

## 🧠 Algorithm

Greedy Best-First Search selects the node with the lowest heuristic value:

```math
f(n) = h(n)
```

where:

- `f(n)` = evaluation function
- `h(n)` = estimated cost from node `n` to the goal

The heuristic used in this project is the **Euclidean Distance**:

```math
h(n)=\sqrt{(x_n-x_{goal})^2+(y_n-y_{goal})^2}
```

A priority queue (Min-Heap) is used to efficiently select the next node to expand.

---

## 📁 Project Structure

```text
greedy-best-first-search-roadnet-ca/
│
├── README.md
├── requirements.txt
├── .gitignore
│
├── src/
│   └── greedy_best_first_search.py
│
├── data/
│   └── roadnet_ca.txt
│
├── docs/
│   └── project_report.pdf
│
├── outputs/
│   └── execution_result.txt
│
└── images/
    └── algorithm_workflow.png
```

---

## 🚀 Getting Started

### Clone the Repository

```bash
git clone https://github.com/your-username/greedy-best-first-search-roadnet-ca.git
```

### Navigate to the Project Directory

```bash
cd greedy-best-first-search-roadnet-ca
```

### Run the Program

```bash
python src/greedy_best_first_search.py
```

---

## 📈 Experimental Results

Example output:

```text
Execution Time: 0.9326 seconds
Expanded Nodes: 403,381

Path Found: Yes
Path Length: 4,857 hops

Route:
[0, 1, 385, 386, 387, ..., 974555]
```

### Key Findings

- The algorithm successfully found a path in a graph containing nearly two million nodes.
- Execution time remained below one second.
- A large number of nodes were expanded due to the limited effectiveness of the heuristic.
- Greedy Best-First Search is fast but does not guarantee an optimal solution.
- Search performance heavily depends on the quality of the heuristic function.

---

## 🛠 Technologies Used

- Python 3
- heapq
- math
- random
- time

---

## 👨‍💻 Team Members

**Group 7**

- Farhanah Hadaya Fatin
- M. Razan Maulana Pratama
- Layina Ropiqo
- Ahmad Bimo Akbar Arkana Putra

Data Science Program

Institut Teknologi Sumatera (ITERA)

---

## 📚 References

1. Stanford Network Analysis Project (SNAP)
2. Russell, S. J., & Norvig, P. *Artificial Intelligence: A Modern Approach*
3. Maulidevi, N. U., & Munir, R. *Route Planning: BFS, DFS, UCS, Greedy Best-First Search*
4. Algorithm Design and Analysis Course Materials

---

## 📄 License

This project is intended for academic and educational purposes only.
