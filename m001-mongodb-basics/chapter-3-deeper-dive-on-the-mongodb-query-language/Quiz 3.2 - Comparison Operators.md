# Comparison Operators

## Problem:
Using the **$in** operator, filter the **video.movieDetails** collection to determine how many movies list either "Ethan Coen" or "Joel Coen" among their writers. Your filter should match all movies that list either of the Coen brothers as writers regardless of how many other writers are also listed. Select the number of movies matching this filter from the choices below.

## Check all that apply:
* 0
* 3
* 7
* 12
* 16

## Answer:
* 3

## Detailed Answer:
ou can find this answer in the mongo shell or in Compass.

In the mongo shell, assuming you've loaded movieDetails into the **video** database and assuming you are connected to your Atlas sandbox cluster, you can issue the following commands.

```
use video

db.movieDetails.find({writers: {$in: ["Ethan Coen", "Joel Coen"]}}).count()
```

In Compass, navigate to the **video.movieDetails** collection in your Atlas sandbox cluster. Then apply the following filter in either the Schema view or Documents view.

```
{writers: {$in: ["Ethan Coen", "Joel Coen"]}}
```