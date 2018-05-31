# Partial Indexes

## Problem:
Which of the following is true regarding partial indexes?

## Check all answers that apply:
1. Partial indexes represent a superset of the functionality of sparse indexes.
2. Partial indexes can be used to reduce the number of keys in an index.
3. Partial indexes don't support a uniqueness constraint.
4. Partial indexes support compound indexes.

## Answer:
1. Partial indexes represent a superset of the functionality of sparse indexes.
2. Partial indexes can be used to reduce the number of keys in an index.
4. Partial indexes support compound indexes.

## Detailed Answer:
All of the following are true:
* Partial indexes represent a superset of the functionality of sparse indexes.
* Partial indexes can be used to reduce the number of keys in an index.
* Partial indexes support compound indexes.

The following is not true:
* Partial indexes don't support a uniqueness constraint.

	No, you can still specify a uniqueness constraint with a partial index. However, uniqueness will be limited to the keys covered by the partial filter expression.