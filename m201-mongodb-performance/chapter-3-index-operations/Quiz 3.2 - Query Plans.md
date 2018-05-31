# Query Plans

## Problem:
Which of the following is/are true concerning query plans?

## Check all answers that apply:
1. MongoDB's query optimizer is statistically based, where collection heuristics are used to determine which plan wins.
2. Query plans are cached so that plans do not need to be generated and compared against each other every time a query is executed.
3. When query plans are generated, for a given query, every index generates at least one query plan.
4. If an index can't be used, then there is no query plan for that query.

## Answer:
2. Query plans are cached so that plans do not need to be generated and compared against each other every time a query is executed.

## Detailed Answer:
* MongoDB's query optimizer is statistically based, where collection heuristics are used to determine which plan wins.

No, MongoDB has an empirical query optimizer where query plans are ran against each other during a trial period.

* Query plans are cached so that plans do not need to be generated and compared against each other every time a query is executed.

Yes, that is correct.

* When query plans are generated, for a given query, every index generates at least one query plan.

No, only a subset of the indexes are considered as candidates for planning.

* If an index can't be used, then there is no query plan for that query.

No, if there aren't any viable indexes for a given query, then a COLLSCAN stage will be the main stage of the query plan.