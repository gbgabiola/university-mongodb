# Challenge Problem: Single Value in an Array of Integers

*This problem is provided as a supplementary learning opportunity. It is somewhat more challenging that the ordinary labs. It is ungraded. We do not ask you submit an answer.*

In the M001 class Atlas cluster you will find a database added just for this week of the course. It is called results. Within this database you will find two collections: **surveys** and **scores**. Documents in the **results.scores** collection have the following schema.

```
{"_id": ObjectId("5964e8e5f0df64e7bc2d7373"), "results": [75, 88, 89]}
```

Connect to our class Atlas cluster from the mongo shell or Compass and view the **results.scores** collection. How many documents contain at least one score in the results array that is greater than or equal to 70 and less than 80?