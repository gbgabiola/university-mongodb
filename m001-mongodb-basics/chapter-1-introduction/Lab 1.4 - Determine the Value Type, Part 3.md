# Lab 1.4: Determine the Value Type, Part 3

## Problem:
What is the value type of the **year** field for documents in the **video.movies** collection?

## Choose the best answer:
1. array
2. coordinates
3. date
4. document
5. double
6. int32
7. mixed string and int32
8. mixed string and double
9. string

## Answer:
6. int32

## Detailed Answer:
In Compass, navigate to the schema view for the **movies** collection of the **video** database. Scroll through the schema view to find the **year** field. The value type is described immediately below the field name. You should see the following for this field in the Compass schema view. Note that **int32** is listed as the value type for **year**.

![video_movies_year_value_type](https://s3.amazonaws.com/edu-static.mongodb.com/lessons/M001/video_movies_year_value_type.png)