# Shaping documents with $project

## Problem:
Which of the following statements are true of the **$project** stage?

## Check all that apply:
1. Once we specify a field to retain or perform some computation in a $project stage, we must specify all fields we wish to retain. The only exception to this is the _id field.
2. Beyond simply removing and retaining fields, $project lets us add new fields.
3. $project can only be used once within an Aggregation pipeline.
4. $project cannot be used to assign new values to existing fields.


## Answer
1. Once we specify a field to retain or perform some computation in a $project stage, we must specify all fields we wish to retain. The only exception to this is the _id field.
2. Beyond simply removing and retaining fields, $project lets us add new fields.

## Detailed Answer:
The correct answers are the following:

* Once we specify a field to retain or perform some computation in a **$project** stage, we must specify all fields we wish to retain. The only exception to this is the **_id** field.

**$project** implicitly removes all other fields once we have retained, reshaped, or computed a new field. The exception to this is the **_id** field, which we must explicitly remove.

* Beyond simply removing and retaining fields, **$project** lets us add new fields.
We can add new fields and reassign the values of existing ones, shaping the documents into different datastructures and computing values using expressions.

The remaining options are incorrect.