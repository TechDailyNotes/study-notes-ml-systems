# Training Pipeline

## Computation-Communication Overlap

1. Problem: After forwarding and backwarding, GPUs need to communicate with each other for All-Reduce accumulation. GPUs are idle, except waiting for result, during this time.
2. Solution: Bucketing - PyTorch splits the model into buckets and send buckets of layers for All-Reduce immediately after backwarding.
