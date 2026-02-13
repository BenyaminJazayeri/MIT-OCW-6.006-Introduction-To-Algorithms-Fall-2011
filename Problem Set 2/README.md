# Min-Heap Priority Queue for Circuit Simulation

Profiled an event-driven digital circuit simulator to identify a performance bottleneck: the `find_min` operation was being called 259,964 times with O(n) worst-case complexity. Replaced the naive priority queue with a min-heap implementation built from scratch, reducing find-min to O(1) and insert/extract to O(log n).

## Implementation

The `PriorityQueue` class provides:

- `min_heapify` — standard sift-down operation to restore the heap invariant
- `append` — insertion with bubble-up (sift-up) to maintain heap order
- `pop` — extract-min by swapping root with last element, then heapifying
- `min` — O(1) peek at the minimum element
- `check_ri` — representation invariant checker for debugging correctness

The surrounding circuit simulator is event-driven, with `TruthTable` (logic gate truth tables), `GateType` (gate types with propagation delays), `Gate` (gates with connections), `Circuit` (topology), `Transition` (output transitions with comparison operators for heap ordering), and `Simulation` (the event loop consuming from the priority queue).
