# Communication Primitives

## Prerequisites

1. GPUs are fully connected. (i.e. GPU cluster is connected by switches)

## Categories

1. Broadcast operator
   1. Definition: Send data (weights/gradients) from 1 GPU to multiple GPUs in the divide-and-conquer strategy.
2. Reduce operator
   1. Definition: Accumulate gradients from multiple GPUs to 1 GPU in the divide-and-conquer strategy.
3. All-Reduce operator
   1. Definition: Reduce operator followed by Broadcast operator.

## Others

1. Ring Topography
   1. Definition: GPUs are connected in a ring topology (topography with 1d torus). Each GPU sends data to the next GPU in the ring.
   2. Ring Reduction
      1. Time Complexity: `O(2*(n-1))` (n is the number of GPUs)
