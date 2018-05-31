# Lab 2.2: Optimizing Compound Indexes

## Problem
In this lab you're going to examine several example queries and determine which compound index will best service them.

```
> db.people.find({
    "address.state": "Nebraska",
    "last_name": /^G/,
    "job": "Police officer"
  })
```

```
> db.people.find({
    "job": /^P/,
    "first_name": /^C/,
    "address.state": "Indiana"
  }).sort({ "last_name": 1 })
```

```
> db.people.find({
    "address.state": "Connecticut",
    "birthday": {
      "$gte": ISODate("2010-01-01T00:00:00.000Z"),
      "$lt": ISODate("2011-01-01T00:00:00.000Z")
    }
  })
```

If you had to build one index on the **people** collection, which of the following indexes would best sevice all 3 queries?

## Check all answers that apply:
1. `{ "job": 1, "address.state": 1, "first_name": 1 }`
2. `{ "job": 1, "address.state": 1, "last_name": 1 }`
3. `{ "address.state": 1, "last_name": 1, "job": 1 }`
4. `{ "job": 1, "address.state": 1 }`
5. `{ "address.state": 1, "job": 1, "first_name": 1 }`
6. `{ "address.state": 1, "job": 1 }`

## Answer:
3. `{ "address.state": 1, "last_name": 1, "job": 1 }`

## Detailed Answer:
The key to this lab is to determine which index will provide the most index prefixes that can be utilized by the 3 example queries.

Let's analyze each option:

* `{ "address.state": 1, "job": 1 }`

No, while this index would be able to service all 3 of the example queries, there's a better index that can be used on the first query, and the second query has to do an in-memory sort.

* `{ "address.state": 1, "job": 1, "first_name": 1 }`

No, this index is better than the first, but it still doesn't help with the sort on the second query.

* `{ "address.state": 1, "last_name": 1, "job": 1 }`

Yes, this is the best index. This index matches the first query, can be used for sorting on the second, and has an prefix for the 3rd query.

* `{ "job": 1, "address.state": 1 }`

No, this index can only be used by the first two queries.

* `{ "job": 1, "address.state": 1, "first_name": 1 }`

No, while this index is better than the one directly above it, this index still cannot be used by the 3rd query at all.

* `{ "job": 1, "address.state": 1, "last_name": 1 }`

No, this index has the same issues as the index directly above it.