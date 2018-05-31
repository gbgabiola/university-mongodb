# Lab 1.6: Scavenger Hunt, Part 2

## Problem:
How many documents in the **citibike.trips** collection have a tripduration that is greater than or equal to 60 and less than 65?

## Choose the best answer:
* 0
* 94
* 216
* 355
* 754

## Answer:
* 754

## Detailed Answer:
In Compass, navigate to either the schema view or the documents view for the **citibike.trips** collection. To get the correct answer, you need to enter the following query in the filter form field:

```
 {"tripduration": {"$gte": 60, "$lt": 65}}
```