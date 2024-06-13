# Pipeline Optimization

## Subminibatches

1. Definition: Divide the data batch assigned to each server into `k` subminibatches, each server process one subminibatch at a time and send it to subsequent server as soon as it finishes processing.
2. Benifits:
   1. Reduce the idle processing time of servers.

## Interleaved Layers

1. Definition: Reuse idle servers/nodes to process next layers of the model.
2. Problems: Not suitable for skip-connection layers/residual layers.
