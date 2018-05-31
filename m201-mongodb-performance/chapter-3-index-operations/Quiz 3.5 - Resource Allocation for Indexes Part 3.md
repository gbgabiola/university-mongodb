# Resource Allocation for Indexes Part 3

## Problem:
Which of the following statements apply to index resource allocation?

## Check all answers that apply:
1. For the fastest processing, we should ensure that our indexes fit entirely in RAM
2. Index information does not need to completely allocated in RAM since MongoDB only uses the right-end-side to the index b-tree, regardless of the queries that use index.
3. Indexes are not required to be entirely placed in RAM, however performance will be affected by constant disk access to retrieve index information.

## Answer:
1. For the fastest processing, we should ensure that our indexes fit entirely in RAM
3. Indexes are not required to be entirely placed in RAM, however performance will be affected by constant disk access to retrieve index information.