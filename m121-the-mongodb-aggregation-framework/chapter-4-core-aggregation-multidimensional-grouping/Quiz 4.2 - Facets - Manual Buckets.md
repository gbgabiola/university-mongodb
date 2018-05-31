# Facets: Manual Buckets

## Problem:
Assuming that **field1** is composed of double values, ranging between 0 and Infinity, and **field2** is of type string, which of the following stages are correct?

## Choose the best answer:
1. `{'$bucket': { 'groupBy': '$field1', 'boundaries': [ "a", 3, 5.5 ]}}`

2. `{'$bucket': { 'groupBy': '$field1', 'boundaries': [ 0.4, Infinity ]}}`

3. `{'$bucket': { 'groupBy': '$field2', 'boundaries': [ "a", "asdas", "z" ], 'default': 'Others'}}`


## Answer
3. `{'$bucket': { 'groupBy': '$field2', 'boundaries': [ "a", "asdas", "z" ], 'default': 'Others'}}`

## Detailed Answer:
The correct answer for this quiz is:

```
{'$bucket': { 'groupBy': '$field2', 'boundaries': [ "a", "asdas", "z" ], 'default': 'Others'}}
```

The other two options will end up in error.

* `{'$bucket': { 'groupBy': '$field1', 'boundaries': [ "a", 3, 5.5 ]}}` will generate inconsistent boundary type error. Boundaries are required to have the same type.
* `{'$bucket': { 'groupBy': '$field1', 'boundaries': [ 0.4, Infinity ]}}` will generate a not matching branch, bucket, to place non matching documents. The **default** stage option would prevent such errors.