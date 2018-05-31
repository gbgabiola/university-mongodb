# Aggregation Performance

## Problem:
With regards to aggregation performance, which of the following are true?

## Check all answers that apply:
1. You can increase index usage by moving $match stages to the end of your pipeline
2. Passing allowDiskUsage to your aggregation queries will seriously increase their performance
3. When $limit and $sort are close together a very performant top-k sort can be performed
4. Transforming data in a pipeline stage prevents us from using indexes in the stages that follow

## Answer:
3. When $limit and $sort are close together a very performant top-k sort can be performed
4. Transforming data in a pipeline stage prevents us from using indexes in the stages that follow

## Detailed Answer:
* **You can increase index usage by moving $match stages to the end of your pipeline**

No, you should move $match stages to the beginning of your pipelines!

* **Passing allowDiskUsage to your aggregation queries will seriously increase their performance**

No, allowDiskUsage will decrease query performance, but it will be necessary to circumvent the 100MB per stage limit.

* **When $limit and $sort are close together a very performant top-k sort can be performed**

Yes, this is true!

* **Transforming data in a pipeline stage prevents us from using indexes in the stages that follow**

Yes, this is true. That's why it's important to put all your index using operators at the front of your pipelines!