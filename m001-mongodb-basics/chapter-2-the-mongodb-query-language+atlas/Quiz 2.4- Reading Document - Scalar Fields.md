# Reading Documents: Scalar Fields

## Problem:
Explore the movieDetails collection that you loaded into your Atlas sandbox cluster and then issue a query to answer the following question. How many movies in the movieDetails collection have exactly 2 award wins and 2 award nominations?

You will find the [count()](https://docs.mongodb.com/manual/reference/method/cursor.count/?_ga=2.49866351.818619118.1525830239-1962173749.1525218334) method useful in answering this question using the mongo shell.

## Choose the best answer:
* 3
* 7
* 12
* 15
* 20

## Answer:
* 12

## Detailed Answer:
You can find this answer in either the mongo shell or in Compass.

In the shell, assuming you've loaded movieDetails into the **video** database and assuming you are connected to your Atlas sandbox cluster, you can issue the following query.

```
db.movieDetails.find({"awards.wins": 2, "awards.nominations": 2}).count()
```

In Compass you can use the following filter in the Documents tab for the movieDetails collection.

```
{awards.wins: 2, awards.nominations: 2}
```