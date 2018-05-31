# The $lookup Stage

## Problem:
Which of the following statements is true about the **$lookup** stage?

## Check all that apply:
1. $lookup matches between localField and foreignField with an equality match
2. You can specify a collection in another database to from
3. Specifying an existing field name to as will overwrite the the existing field
4. The collection specified in from cannot be sharded


## Answer
1. $lookup matches between localField and foreignField with an equality match
3. Specifying an existing field name to as will overwrite the the existing field
4. The collection specified in from cannot be sharded

## Detailed Answer:
The only false statement is:

* You can specify a collection in another database to **from**
This is not true, you can only specify another collection to **from** within the same database.

All other statements are true.