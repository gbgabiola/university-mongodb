# Lab 2.4: Queries on Array Fields, Part 1

## Problem:
Explore the movieDetails collection that you loaded into your Atlas sandbox cluster and then issue a query to answer the following question. How many movies in the movieDetails collection list "Family" among its genres?

You will find the [count()](https://docs.mongodb.com/manual/reference/method/cursor.count/?_ga=2.82709087.818619118.1525830239-1962173749.1525218334) method useful in answering this question using the mongo shell.

## Choose the best answer:
* 20
* 57
* 124
* 200
* 277

## Answer:
* 124

## Detailed Answer:
You can find this answer in either the mongo shell or in Compass.

In the shell, assuming you've loaded movieDetails into the **video** database and assuming you are connected to your Atlas sandbox cluster, you can issue the following query.

```
db.movieDetails.find({genres: "Family"}).count()
```

In Compass you can use the following filter in the Documents tab for the movieDetails collection.

```
{genres: "Family"}
```