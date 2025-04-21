
# UAV Structure Inspection: Path Planning (TSP Version)

This repository is part of the *UAV Structure Inspection* research project, focusing on static path planning for indoor and outdoor structural scanning. The notebook `Path_planning_tsp.ipynb` demonstrates the use of MST (Minimum Spanning Tree) and TSP (Travelling Salesman Problem) algorithms to generate efficient inspection paths from point cloud data.

---

## 📘 File Overview

### `Path_planning_tsp.ipynb`
- Loads selected surface points from point cloud data
- Constructs a graph based on valid connectivity (e.g., no obstacles)
- Applies:
  - **MST** to build a connected backbone
  - **TSP** to optimize path order
- Visualizes the final planned path using `matplotlib`

---

## 🧠 Techniques Used
- **Graph construction** from 2D/3D point sets
- **Prim’s algorithm** or `networkx.minimum_spanning_tree()`
- **TSP heuristic** via `networkx.approximation.traveling_salesman_problem()`
- **Matplotlib** for path visualization

---

## 🏁 Getting Started

### Requirements
```bash
pip install numpy networkx matplotlib
```

### Run locally
1. Clone the repo
2. Launch Jupyter Notebook
3. Open `Path_planning_tsp.ipynb` and run cells

---

## 📌 Notes
- Input point set should be pre-processed surface points (e.g., from Delaunay or Hough Transform)
- Obstacles should already be filtered out; future versions may support collision checking

---

## ✏️ To-Do
- Integrate with point cloud input pipeline
- Add visibility constraints based on camera FOV
- Compare with alternative algorithms (e.g., RRT, FUEL)

---

## 🧑‍💻 Author
Wen-Chi Tsai — [GitHub](https://github.com/vicky0619)

---

## 📜 License
For academic use only. Developed under a research project commissioned by Chunghwa Telecom.
```
