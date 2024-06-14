# Machine Learning Systems

## Parallelism

1. Data Parallelism (DDP - Distributed Data Parallelism)
   1. Scenario: If the model fits in a single GPU, but the dataset is too large to fit in a single GPU.
2. Model Parallelism
   1. Scenario: If the model is too large to fit in a single GPU.

## Network Topologies

1. Switched Network / Fully Connected Network
   1. Definition: Each node is connected to a switch.
2. Ring Network
   1. Definition: Each node is connected to two other nodes forming a ring.
3. Mesh Network
   1. Definition: Each node is connected to four other nodes forming a mesh.
