# Databases, Collections, and Documents

## Problem:
Which of the following statements are true? Check all that apply.

## Check all answers that apply:
1. Documents are stored in collections.
2. A database may contain one or more collections.
3. Each database and collection combination define a namespace.
4. We reference a namespace using the name of the database, followed by a comma, followed by the name of the collection, e.g., city,neighborhoods.
5. We won't talk about indexes too much in the course, but you can learn about indexes in M201: MongoDB Performance.

## Answer:
1. Documents are stored in collections.
2. A database may contain one or more collections.
3. Each database and collection combination define a namespace.
5. We won't talk about indexes too much in the course, but you can learn about indexes in M201: MongoDB Performance.

## Detailed Answer:
All statements except one are true. While we do reference a namespace using a combination of the name of the database and collection, we use a dot (".") not a comma to separate the database and collection names in a namespace, e.g., **city.neighborhoods**.