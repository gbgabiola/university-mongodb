# Understanding Explain Part 2

## Problem:
With the output of an explain command, what can you deduce?

## Check all answers that apply:
1. The index used by the chosen plan
2. If a sort was performed by walking the index or done in memory
3. All the available indexes for this collection
4. All the different stages the query needs to go through with details about the time it takes, the number of documents processed and returned to the next stage in the pipeline
5. The estimation of the cardinalities of the distribution of the values

## Answer:
1. The index used by the chosen plan
2. If a sort was performed by walking the index or done in memory
4. All the different stages the query needs to go through with details about the time it takes, the number of documents processed and returned to the next stage in the pipeline

## Detailed Answer:
* The index used by the chosen plan

Yes, additional information will be the direction the index is used, the bounds of the values looked at and the number of keys examined.

* If a sort was performed by walking the index or done in memory

Yes.

* All the available indexes for this collection

No, you will be able to see the ones considered by the other plans that were rejected with the "allExecutionPlans" option, but this is possibly only a subset of all indexes.

* All the different stages the query needs to go through with details about the time it takes, the number of documents processed and returned to the next stage in the pipeline

Yes.

* The estimation of the cardinalities of the distribution of the values

No, while some RDBMS use this kind of statistics to select indexes, MongoDB executes all select plans for a short duration of time and picks the best based on execution results.