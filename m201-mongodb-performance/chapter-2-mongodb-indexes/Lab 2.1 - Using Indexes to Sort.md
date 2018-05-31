# Lab 2.1: Using Indexes to Sort

## Problem
In this lab you're going to determine which queries are able to successfully use a given index for both filtering and sorting.

Given the following index:

```
{ "first_name": 1, "address.state": -1, "address.city": -1, "ssn": 1 }
```

Which of the following queries are able to use it for both filtering and sorting?

## Check all answers that apply:
1. db.people.find({ "address.state": "South Dakota", "first_name": "Jessica" }).sort({ "address.city": -1 })
2. db.people.find({ "address.city": "West Cindy" }).sort({ "address.city": -1 })
3. db.people.find({ "first_name": "Jessica", "address.state": { $lt: "S"} }).sort({ "address.state": 1 })
4. db.people.find({ "first_name": "Jessica" }).sort({ "address.state": 1, "address.city": 1 })
5. db.people.find({ "first_name": { $gt: "J" } }).sort({ "address.city": -1 })

## Answer:
1. db.people.find({ "address.state": "South Dakota", "first_name": "Jessica" }).sort({ "address.city": -1 })
3. db.people.find({ "first_name": "Jessica", "address.state": { $lt: "S"} }).sort({ "address.state": 1 })
4. db.people.find({ "first_name": "Jessica" }).sort({ "address.state": 1, "address.city": 1 })

## Detailed Answer:
The key to this lab is to identify the prefixes for the given index, and to take your time and think about each query one by one.

Here's an explanation for each query:

* **db.people.find({ "first_name": { $gt: "J" } }).sort({ "address.city": -1 })**

No, this query doesn't use equality on the index prefix. When using an index for filtering and sorting the query must include equality conditions on all the prefix keys that precede the sort keys. Moreover, on the sort predicate it skipped the next key in the prefix **"address.state"**.

* **db.people.find({ "first_name": "Jessica" }).sort({ "address.state": 1, "address.city": 1 })**

Yes, this query matches with equality on the query predicate with an index prefix, and continues the prefix in the sort predicate by walking the index backward.

* **db.people.find({ "first_name": "Jessica", "address.state": { $lt: "S"} }).sort({ "address.state": 1 })**

Yes, while this query fails to use equality on the "address.state" field of the index prefix, it uses the same field for sorting.

* **db.people.find({ "address.city": "West Cindy" }).sort({ "address.city": -1 })**

No, this query does not use an index prefix.

* ** db.people.find({ "address.state": "South Dakota", "first_name": "Jessica" }).sort({ "address.city": -1 })**

Yes, this query is able to use the index prefix. The order of the fields in the query predicate does not matter.