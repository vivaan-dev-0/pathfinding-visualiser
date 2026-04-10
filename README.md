# Pathfinding Lab 

An interactive, browser-based pathfinding algorithm visualiser built from scratch with vanilla HTML, CSS and JavaScript. Designed to demonstrate how classic graph search algorithms explore a grid and find the shortest path between two points.

>  [Live Demo](https://vivaan-dev-0.github.io/pathfinding-visualiser)

---

## Algorithms

| Algorithm | Optimal? | Strategy |
|---|---|---|
| **A\*** | ✅ Yes | Heuristic-guided — balances cost so far and estimated cost to goal |
| **Dijkstra** | ✅ Yes | Explores by lowest cumulative cost — guaranteed shortest path |
| **BFS** | ✅ Yes (unweighted) | Expands layer by layer — shortest path on uniform grids |
| **Greedy Best-First** | ❌ No | Darts toward the goal using only the heuristic — fast but non-optimal |
| **DFS** | ❌ No | Explores as deep as possible before backtracking |
| **Bidirectional BFS** | ✅ Yes (unweighted) | Searches simultaneously from start and end — meets in the middle |

---

## Features

- **Interactive grid** — click and drag to draw walls, place start/end points, and add obstacles
- **Moving obstacles** — place and drag obstacles around the grid in real time
- **Step-by-step mode** — advance the algorithm one node at a time to understand exactly how it works
- **Animated visualisation** — watch the frontier expand and the final path trace back
- **Adjustable speed** — slow down or speed up the animation with a slider
- **Maze generation** — generates a random perfect maze using recursive backtracking (path always guaranteed)
- **Live stats** — tracks nodes visited, path length, and execution time per run
- **Multiple grid sizes** — from 20×15 up to 50×30
- **Fully offline** — single `.html` file, no dependencies, no build step

---

## How to Use

###Run locally
1. Download `pathfinding_visualiser.html`
2. Open it in any modern browser (Chrome, Firefox, Edge)
3. No installation required

### Run in Google Colab
1. Upload `Pathfinding_Lab.ipynb` to [Google Colab](https://colab.research.google.com)
2. Upload `pathfinding_visualiser.html` using the Files panel (folder icon, left sidebar)
3. Run the first cell — the visualiser loads inline in the notebook

---

## Controls

| Action | How |
|---|---|
| Draw wall | Select **Wall** tool, click/drag on grid |
| Set start point | Select **Start** tool, click a cell |
| Set end point | Select **End** tool, click a cell |
| Add moving obstacle | Select **Moving Obstacle** tool, click a cell |
| Drag moving obstacle | Select **Moving Obstacle** tool, drag an existing obstacle |
| Erase cell | Select **Erase** tool, click a cell |
| Run algorithm | Click **▶ Visualise** |
| Step through | Click **Step →** repeatedly |
| Generate maze | Click **Random Maze** |
| Clear path only | Click **Clear Path** |
| Reset everything | Click **Clear All** |

---

## Implementation Notes

- **A\*** uses Manhattan distance as the heuristic with a closed set to prevent re-expansion of settled nodes
- **Dijkstra** uses a priority queue sorted by cumulative cost with a visited set
- **Bidirectional BFS** expands from both start and end simultaneously and reconstructs the path at the meeting point
- **DFS** records parent pointers at pop-time (not push-time) to avoid path corruption from stack ordering
- **Maze generation** uses recursive backtracking — guarantees a perfect maze where every cell is reachable

---

## Built With

- Vanilla JavaScript (no frameworks or libraries)
- HTML5 Canvas for grid rendering
- CSS custom properties for theming
- Python (Google Colab notebook companion)

---

## Author

**vivaananand** — Computer Science student  
[GitHub](https://github.com/vivaan-dev-0) · [Live Demo](https://vivaan-dev-0.github.io/pathfinding-visualiser)
