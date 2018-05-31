# Facets: Auto Buckets

## Problem:
Auto Bucketing will ...

## Check all answers that apply:
1. given a number of buckets, try to distribute documents evenly accross buckets.
2. adhere bucket boundaries to a numerical series set by the **granularity** option.
3. randomly distributed documents accross arbitrarily defined bucket boundaries.
4. count only documents that contain the **groupBy** field defined in the documents.

## Answer
1. given a number of buckets, try to distribute documents evenly accross buckets.
2. adhere bucket boundaries to a numerical series set by the **granularity** option.

## Detailed Answer:
The two correct options are:

* Auto Bucketing will, given a number of buckets, try to distribute documents evenly across buckets.
* Auto Bucketing will adhere bucket boundaries to a numerical series set by the **granularity** option

Auto bucketing facets, defined using **$bucketAuto** stage, will generate buckets accordingly with the number of buckets requested, **buckets** field, distributing the documents evenly across those buckets, by default.

In case we define a **granularity** for this stage, it will use the specified numerical series to determined the boundaries of the buckets and generate buckets according with those boundaries.