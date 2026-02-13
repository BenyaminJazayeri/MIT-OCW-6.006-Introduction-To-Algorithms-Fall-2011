# BST / AVL / Range Tree + Sweep Line Circuit Layout

A full balanced tree hierarchy built from scratch, used as the backing data structure for a sweep line algorithm that detects wire crossings in digital circuit layouts. Replaced an O(n²) brute-force approach (187 million `intersects` calls) with O(n log n).

## Implementation

### `bst.py` — Binary Search Tree

`BSTNode` with `find`, `find_min`, `next_larger`, `insert`, `delete`, and `check_ri` (representation invariant checker). Includes ASCII art tree visualization via `_str`. `MinBSTNode` extends `BSTNode` with a `min` pointer that propagates on insert and delete for O(1) minimum access. `BST` and `MinBST` wrapper classes manage the root.

### `avl.py` — AVL Tree

Extends the BST with self-balancing through `left_rotate` and `right_rotate` operations. The `rebalance` method walks up from a node, performing rotations as needed to maintain the AVL height invariant across all four cases (left-left, left-right, right-left, right-right). Overrides `insert` and `delete` to call `rebalance` after the BST operation.

### `range_tree.py` — Size-Augmented Range Tree

Extends the AVL tree with subtree size augmentation, updated on rotations and rebalancing. Supports:

- `rank(k)` — counts elements smaller than k using subtree sizes, O(log n)
- `count(l, h)` — range count via `rank(h) - rank(l)`, O(log n)
- `lca(l, h)` — lowest common ancestor for range queries
- `list(l, h)` — enumerates all keys in range [l, h]

### `circuit2.py` — Sweep Line Wire Crossing Detection

Uses the range tree as a `RangeIndex` for a sweep line algorithm. Creates events (add/remove/query) sorted by x-coordinate, sweeps left to right, and uses the range index to efficiently count and list crossings between horizontal and vertical wires. `Wire`, `WireLayer`, `CrossVerifier`, and `KeyWirePair` classes manage the geometry and sweep state.
