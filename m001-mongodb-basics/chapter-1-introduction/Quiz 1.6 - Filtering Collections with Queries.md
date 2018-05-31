# Filtering Collections with Queries

## Problem:
Which of statements below best describes the following filter?

```
 {"age": {"$gte": 21, "$lt": 70}}
```

## Choose the best answer:
1. Find all documents for which the **age** field has a value that is >= 21 and <= 70.
2. Find all documents for which the **age** field has a value that is either equal to 21 or equal to 70.
3. Find all documents for which the **age** field has a value that is >= 21 and < 70.
4. Find all documents for which the **age** field is < 70.
5. None of the above.

## Answer:
3. Find all documents for which the **age** field has a value that is >= 21 and < 70.

## Detailed Answer:
MongoDB's query language is based on documents. In this case, we are specifying a range query on the age field. Specifically, we are looking for documents where the **age** is >= ("$gte") 21 and < ("$lt") 70.