# The Concept of Pipelines

## Problem:
Which of the following is/are true of the $match stage?

## Check all that apply:
1. $match can use both query operators and aggregation expressions.
2. $match can only filter documents on one field.
3. It should come very early in an aggregation pipeline.
4. It uses the familiar MongoDB query language.


## Answer
3. It should come very early in an aggregation pipeline.
4. It uses the familiar MongoDB query language.

## Detailed Answer:
The correct answers are:

* It uses the familiar MongoDB query language.
**$match** uses the MongoDB query language query operators to express queries.

* It should come very early in an aggregation pipeline.
The earlier in the pipeline, the more efficient our pipelines will become. Not only because we will expression filters that reduce the number of documents to process, but also the fact that we might be using indexes withing the pipeline execution.

The remaining options are not correct.