# Lab 1.5: Scavenger Hunt, Part 1

## Problem:
How many movies in the video collection were directed by Patty Jenkins. Stated more precisely, how many documents in the video.movies collection have a value of "Patty Jenkins" for the director field?

## Choose the best answer:
* 6
* 13
* 47
* 98
* 143

## Answer:
* 6

## Detailed Answer:
In Compass, navigate to either the schema view or the documents view for the **movies** collection of the **video** database. To get the correct answer, you need to enter the following query in the filter form field:

```
 {"director": "Patty Jenkins"}
```