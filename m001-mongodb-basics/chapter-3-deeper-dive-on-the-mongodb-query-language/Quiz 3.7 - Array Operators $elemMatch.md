# Array Operators: $elemMatch

## Problem:
In the M001 class Atlas cluster you will find a database added just for this week of the course. It is called results. Within this database you will find two collections: **surveys** and **scores**. Documents in the **results.surveys** collection have the following schema.

```
 {_id: ObjectId("5964e8e5f0df64e7bc2d7373"),
 results: [{product: "abc", score: 10}, {product: "xyz", score: 9}]}
```
The field called **results** that has an array as its value. This array contains survey results for products and lists the product name and the survey score for each product.

How many documents in the **results.surveys** collection contain a score of 7 for the product, "abc"?

## Choose the best answer:
* 35
* 124
* 172
* 220
* 301

## Answer:
* 124

## Detailed Answer:
You can find this answer in the mongo shell or in Compass.

In the mongo shell, assuming you've connected to the M001 class Atlas cluster, you can issue the following commands to find this value.

```
use results

db.surveys.find({results: {$elemMatch: {product: "abc", score: 7}}}).count()
```

Note that it is incorrect to use the following query.

```
db.surveys.find({"results.product": "abc", "results.score": 7})
```

because in addition to correct results, this will return the document.

```
{"_id": 4, "results": [{"product": "abc", "score": 8}, {"product": "xyz", "score": 7}]}
```

This document does contain an entry for "abc" and a score of 7 in the results array, but the 7 is the score of the "xyz" product, not "abc".

In Compass, navigate to the **results.surveys** collection and then apply the following filter in either the Schema or Documents view.

```
{results: {$elemMatch: {product: "abc", score: 7}}}
```