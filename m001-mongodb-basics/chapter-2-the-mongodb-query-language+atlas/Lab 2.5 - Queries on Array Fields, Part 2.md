# Lab 2.5: Queries on Array Fields, Part 2

## Problem:
Explore the movieDetails collection that you loaded into your Atlas sandbox cluster and then issue a query to answer the following question. How many movies in the movieDetails collection list "Western" second among its genres?

You will find the [count()](https://docs.mongodb.com/manual/reference/method/cursor.count/?_ga=2.69848665.818619118.1525830239-1962173749.1525218334) method useful in answering this question using the mongo shell.

## Choose the best answer:
* 7
* 14
* 80
* 93
* 102

## Answer:
* 14

## Detailed Answer:
You can find this answer in either the mongo shell or in Compass.

In the shell, assuming you've loaded movieDetails into the **video** database and assuming you are connected to your Atlas sandbox cluster, you can issue the following query.

```
db.movieDetails.find({"genres.1": "Western"}).count()
```

In Compass you can use the following filter in the Documents tab for the movieDetails collection.

```
{genres.1: "Western"}
```