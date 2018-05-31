# Reading Documents: Array Fields

## Problem:
Explore the movieDetails collection that you loaded into your Atlas sandbox cluster and then issue a query to answer the following question. How many documents list just two writers: "Ethan Coen" and "Joel Coen", in that order?

You will find the count() method useful in answering this question using the mongo shell.

## Choose the best answer:
* 1
* 3
* 7
* 12
* 20

## Answer:
* 1

## Detailed Answer:
You can find this answer in either the mongo shell or in Compass.

In the shell, assuming you've loaded movieDetails into the **video** database and assuming you are connected to your Atlas sandbox cluster, you can issue the following query.

```
db.movieDetails.find({writers: ["Ethan Coen", "Joel Coen"]}).count()
```

In Compass you can use the following filter in the Documents tab for the movieDetails collection.

```
{writers: ["Ethan Coen", "Joel Coen"]}
```