# Final Exam: Question 5

## Problem:
Using the **video.movieDetails** collection, which of the queries below would produce output documents that resemble the following. Check all that apply.

```
{ "title" : "P.S. I Love You" }
{ "title" : "Love Actually" }
{ "title" : "Shakespeare in Love" }
```

NOTE: We are not asking you to consider specifically which documents would be output from the queries below, but rather what fields the output documents would contain.

## Check all that apply:
1. db.movieDetails.find({year: 1964}, {title: 1, _id: 0})
2. db.movieDetails.find({title: "Muppets from Space"}, {title: 1})
3. db.movieDetails.find({title: ""}, {title: 1})
4. db.movieDetails.find({}, {title})
5. db.movieDetails.find({}, {title: 1})
6. db.movieDetails.find({}, {title: 1, _id: 0})

## Answer:
1. db.movieDetails.find({year: 1964}, {title: 1, _id: 0})
6. db.movieDetails.find({}, {title: 1, _id: 0})

## Detailed Answer:
