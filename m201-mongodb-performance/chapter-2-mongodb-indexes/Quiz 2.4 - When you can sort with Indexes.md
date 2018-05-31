# When you can sort with Indexes

## Problem:
Which of the following statements are true?

## Check all answers that apply:
1. Index prefixes can be used in query predicates to increase index utilization.
2. Index prefixes can be used in sort predicates to prevent in-memory sorts.
3. We can invert the keys of an index in our sort predicate to utilize an index by walking it backwards.
4. It's impossible to have a sorted query use an index for both sorting and filtering.

## Answer:
1. Index prefixes can be used in query predicates to increase index utilization.
2. Index prefixes can be used in sort predicates to prevent in-memory sorts.
3. We can invert the keys of an index in our sort predicate to utilize an index by walking it backwards.

## Detailed Answer:
**It's impossible to have a sorted query use an index for both sorting and filtering.**

	No, if our sort keys are a non-prefix subset of the index key pattern and the query includes equality conditions on all the prefix keys that precede the sort keys we can use the index for both sorting and filtering.
	
All of the following are true:
* Index prefixes can be used in query predicates to increase index utilization.
* Index prefixes can be used in sort predicates to prevent in-memory sorts.
* We can invert the keys of an index in our sort predicate to utilize an index by walking it backwards.