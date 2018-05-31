# Facets: Multiple Facets

## Problem:
Which of the following statement(s) apply to the **$facet** stage?

## Check all answers that apply:
1. The $facet stage allows several sub-pipelines to be executed to produce multiple facets.
2. The $facet stage allows the application to generate several different facets with one single database request.
3. The output of the individual $facet sub-pipelines can be shared using the expression $$FACET.$.
4. We can only use facets stages ($sortByCount, $bucket and $bucketAuto) as sub-pipelines of $facet stage.

## Answer
1. The $facet stage allows several sub-pipelines to be executed to produce multiple facets.
2. The $facet stage allows the application to generate several different facets with one single database request.

## Detailed Answer:
The correct answers are:

* The **$facet** stage allows several sub-pipelines to be executed to produce multiple facets.
* The **$facet** stage allows the applications to generate several different facets with one single database request.

The **$facet** stage allows other stages to be included on the sub-pipelines, except for:
* $facet
* $out
* $geoNear
* $indexStats
* $collStats

Also, the sub-pipelines, defined for each individual facet, cannot share their output accross other parallel facets. Each sub-pipeline will receive the same input data set but does not share the result dataset with parallel facets.