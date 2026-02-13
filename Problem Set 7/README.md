# Content-Aware Image Resizing with Dynamic Programming (Seam Carving)

A dynamic programming implementation of the [Avidan & Shamir](https://www.youtube.com/watch?v=vIFCV2spKtg) seam carving algorithm for content-aware image resizing.

## Implementation

- `best_seam()` — bottom-up dynamic programming over the image grid. Creates a 2D DP table with sentinel infinity values on left and right borders to handle boundary cases. For each pixel (i, j), computes the minimum-energy path from the top row to that pixel. Each entry stores a tuple of (total energy, backpointer coordinates, current coordinates). Finds the minimum in the bottom row, then traces back through backpointers to reconstruct the full minimum-energy vertical seam
- `remove_best_seam()` — calls `best_seam()` to find the optimal seam, then delegates to the inherited `remove_seam()` method to strip those pixels from the image
