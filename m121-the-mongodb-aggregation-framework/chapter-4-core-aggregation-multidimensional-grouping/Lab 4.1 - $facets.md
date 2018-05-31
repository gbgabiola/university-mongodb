# Lab 4.1: $facets

## Problem:
How many movies are in both the top ten highest rated movies according to the **imdb.rating** and the **metacritic** fields? We should get these results with exactly one access to the database.

**HINT**: What is the _intersection_?

## Choose the best answer:
* 1
* 2
* 5
* 3

## Answer:
* 1

## Detailed Answer:

```
db.movies.aggregate([
  {
    $match: {
      metacritic: { $gte: 0 },
      "imdb.rating": { $gte: 0 }
    }
  },
  {
    $project: {
      _id: 0,
      metacritic: 1,
      "imdb.rating": 1,
      title: 1
    }
  },
  {
    $facet: {
      topMetacritic: [
        {
          $sort: {
            metacritic: -1
          }
        },
        {
          $limit: 10
        },
        {
          $project: {
            title: 1
          }
        }
      ],
      topImdb: [
        {
          $sort: {
            "imdb.rating": -1
          }
        },
        {
          $limit: 10
        },
        {
          $project: { title: 1 }
        }
      ]
    }
  },
  {
    $project: {
	result: {
        $setIntersection: ["$topMetacritic", "$topImdb"]
      }
    }
  },
  {
	$count: "result" 
  }
])
```