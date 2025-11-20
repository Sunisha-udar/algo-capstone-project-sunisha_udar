# algo-capstone-project-sunisha_udar
📦 **Delivery Network Optimization**

**Minimum Spanning Tree (MST) + Traveling Salesman Problem (TSP) + Profiling**

This project analyzes a small delivery network of warehouses (C1, C2, C3, …) and computes:

**Minimum Spanning Tree (MST) using**
✔ Kruskal’s Algorithm

✔ Prim’s Algorithm

**Traveling Salesman Problem (TSP)**
✔ Backtracking (Optimal for small n)

✔ Heuristic distance-based selection

**Experimental profiling**
✔ Execution time

✔ Memory usage

**Graph visualizations**
✔ Delivery network

✔ MST overlay

✔ TSP route sequence

The notebook is fully modular and organized cell-by-cell.

🔧 **Features Implemented**
**1. Delivery Network Setup**

Nodes represent warehouse locations (C1, C2, C3…)

Distances computed using Euclidean distance

Fully connected graph constructed using NetworkX

🌲 **2. Minimum Spanning Tree (MST)**

MST is computed using:

✔ **Kruskal’s Algorithm**

Sort all edges by weight

Pick edges that do not form cycles (Union–Find)

✔ **Prim’s Algorithm**

Start from first warehouse (C1)

Grow MST by repeatedly selecting shortest edge to an unvisited node

Both algorithms return:

List of MST edges

Total MST cost

Comparison to ensure correctness

Visualization

Blue nodes

Black edges

MST highlighted using light blue, thicker edges

🛣 **3. Traveling Salesman Problem (TSP)**

**Two versions:**

✔ **Backtracking (Exact Optimal)**

Explores all permutations with pruning

Only suitable for small n (≤10)

✔ **Heuristic (Greedy Nearest Neighbor)**

Starts at the first warehouse

Always goes to the nearest unvisited warehouse

Much faster but not always optimal

TSP Output

Full optimal route

Total route cost

Route visualized using yellow line with black outline markers

📈 **4. Experimental Profiling**

To compare computational efficiency:

✔ **Execution Time**

Measured using time.time().

✔ **Memory Usage**

Measured using memory_profiler.memory_usage().

The profiling graph shows:

How time increases with added nodes

Difference between MST (very fast) vs TSP (explodes quickly)

📊 **5. Visualizations**
Graphs Included

Complete delivery network graph

Nodes = warehouses

Edge labels = distances

MST overlay in thick light blue

TSP route progression plot

Yellow markers

Black marker edges

White background

Profiling charts

Time vs number of nodes

Memory vs number of nodes


🚀 **How to Run**

**Install dependencies:**

pip install networkx matplotlib memory_profiler numpy


**Open the notebook:**

jupyter notebook


**Run cells in order:**

Graph setup

MST

TSP

Profiling

Visualizations

📌 **Notes**

Backtracking TSP grows factorially → Only use for small networks (3–9 warehouses).

MST is extremely fast and scalable.

Visualizations are customizable (node colors, MST color, TSP path color, layout, etc.)

🔚 **Conclusion**

This project demonstrates how graph theory optimizes delivery logistics by:

Minimizing infrastructure cost (MST)

Minimizing travel cost (TSP)

Evaluating algorithm efficiency (profiling)

It provides both accurate algorithms and clear visual insights into the delivery network.
