# Lab 2.3: Queries on Scalar Fields

## Problem:
Explore the movieDetails collection that you loaded into your Atlas sandbox cluster and then issue a query to answer the following question. How many movies in the movieDetails collection are rated PG and have exactly 10 award nominations?

You will find the [count()](https://docs.mongodb.com/manual/reference/method/cursor.count/?_ga=2.70820185.818619118.1525830239-1962173749.1525218334) method useful in answering this question using the mongo shell.

## Choose the best answer:
* 0
* 1
* 3
* 6
* 11

## Answer:
* 3

## Detailed Answer:
ou can find this answer in either the mongo shell or in Compass.

In the shell, assuming you've loaded movieDetails into the **video** database and assuming you are connected to your Atlas sandbox cluster, you can issue the following query.

```
db.movieDetails.find({rated: "PG", "awards.nominations": 10}).count()
```

In Compass you can use the following filter in the Documents tab for the movieDetails collection.

```
{rated: "PG", awards.nominations: 10}
```