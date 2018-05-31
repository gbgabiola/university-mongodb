# Facets: Single Facet Query

## Problem:
Which of the following aggregation pipelines are single facet queries?

## Check all answers that apply:
1. `[
  {"$match": { "$text": {"$search": "network"}}},
  {"$sortByCount": "$offices.city"},
]`

2. `[
  {"$unwind": "$offices"},
  {"$project": { "_id": "$name", "hq": "$offices.city"}},
  {"$sortByCount": "$hq"},
  {"$sort": {"_id":-1}},
  {"$limit": 100}
]`

3. `[
  {"$match": { "$text": {"$search": "network"}}},
  {"$unwind": "$offices"},
  {"$sort": {"_id":-1}}
]`


## Answer
1. `[
  {"$match": { "$text": {"$search": "network"}}},
  {"$sortByCount": "$offices.city"},
]`

2. `[
  {"$unwind": "$offices"},
  {"$project": { "_id": "$name", "hq": "$offices.city"}},
  {"$sortByCount": "$hq"},
  {"$sort": {"_id":-1}},
  {"$limit": 100}
]`

## Detailed Answer:
Single query facets are supported by the new aggregation pipeline stage **$sortByCount**.

As like any other aggregation pipelines, except for **$out**, we can use the output of this stage, as input for downstream stages and operators, manipulating the dataset accordingly.

The **correct** answers are:

```
[
  {"$match": { "$text": {"$search": "network"}}},
  {"$sortByCount": "$offices.city"},
]
```

and

```
[
  {"$unwind": "$offices"},
  {"$project": { "_id": "$name", "hq": "$offices.city"}},
  {"$sortByCount": "$hq"},
  {"$sort": {"_id":-1}},
  {"$limit": 100}
]
```

The pipeline

```
[
  {"$match": { "$text": {"$search": "network"}}},
  {"$unwind": "$offices"},
  {"$sort": {"_id":-1}}
]
```

is **not** a single query **facet** since it does not group any particular data dimension. It simply unwinds an array field and sorts that result set.