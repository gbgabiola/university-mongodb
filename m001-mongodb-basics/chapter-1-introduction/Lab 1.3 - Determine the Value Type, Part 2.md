# Lab 1.3: Determine the Value Type, Part 2

## Problem:
What is the value type of the **airTemperature** field for documents in the **100YWeatherSmall.data** collection?

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

## Anwer:
4. document

## Detailed Answer:
In Compass, navigate to the schema view for the **data** collection of the **100YWeatherSmall** database. Scroll through the schema view to find the **airTemperature** field. The value type is described immediately below the field name. You should see the following for this field in the Compass schema view. Note that **document** is listed as the value type for **airTemperature**.

![100yweather_airtemperature_value_type](https://s3.amazonaws.com/edu-static.mongodb.com/lessons/M001/100yweather_airtemperature_value_type.png)