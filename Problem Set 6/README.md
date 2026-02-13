# Dijkstra's Algorithm on the US Highway Network

Dijkstra's shortest-path algorithm applied to the National Highway Planning Network with great-circle distance and KML output for Google Earth visualization.

## Implementation

- `distance` — flat-earth Euclidean distance in latitude/longitude
- `distance_curved` — great-circle distance using the arccosine formula
- `NodeDistancePair` — priority queue key wrapping a node and its distance, with full comparison operators
- `Network` — loads the NHPN dataset, creates adjacency lists and edge sets
- `PathFinder` — contains the core `dijkstra` method using a priority queue with `insert`, `extract_min`, and `decrease_key`. Maintains a `parent` dict for path reconstruction and stops early when the destination is reached
- `PathResult` — formats results including KML output for Google Earth visualization
- Command-line interface supporting flat/curved distance modes, KML output, and solution display

---

# Rubik's Cube Bidirectional BFS Solver

A bidirectional BFS solver for the 2x2x2 Rubik's cube that explores from both start and goal states simultaneously, using permutation group inverses to reconstruct the solution path.

## Implementation

- `BFS_step(frontier, parent)` — expands one level of BFS by applying all quarter-twist permutations to each state in the frontier and recording newly discovered states
- `shortest_path(start, end)` — maintains separate forward and backward frontiers with parent dicts, alternating expansion for 7 iterations. When a state appears in both parent dicts, reconstructs the path by walking backward to `start` and forward to `end` using `perm_inverse`
