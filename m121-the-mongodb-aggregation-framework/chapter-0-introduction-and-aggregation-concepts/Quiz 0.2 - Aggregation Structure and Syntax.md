# Aggregation Structure and Syntax

## Problem:
Which of the following statements is true?

## Check all that apply:
1. Only one expression per stage can be used.
2. Some expressions can only be used in certain stages.
3. An aggregation pipeline is an array of stages.


## Answer
2. Some expressions can only be used in certain stages.
3. An aggregation pipeline is an array of stages.

## Detailed Answer:
In this quiz, we have the following correct answers:

* An aggregation pipeline is an array of stages.
This is correct.

* Some expressions can only be used in certian stages.
This is correct. For example, accumulator expressions can only be used within the **$group** stage, with select accumulator expressions available in the **$project** stage. You'll learn about these stages in depth in the course!

The other option is incorrect:

* Only one expression per stage can be used.
This is not correct. Multiple expressions can be used.