# Data Parallelism

## Communication Primitives

1. Broadcast operator
   1. Definition: Send data (weights/gradients) from 1 GPU to multiple GPUs in the divide-and-conquer strategy.
2. Reduce operator
   1. Definition: Accumulate gradients from multiple GPUs to 1 GPU in the divide-and-conquer strategy.
3. All-Reduce operator
   1. Definition: Reduce operator followed by Broadcast operator.

## Computation-Communication Overlap

1. Problem: After forwarding and backwarding, GPUs need to communicate with each other for All-Reduce accumulation. GPUs are idle, except waiting for result, during this time.
2. Solution: Bucketing - PyTorch splits the model into buckets and send buckets of layers for All-Reduce immediately after backwarding.
