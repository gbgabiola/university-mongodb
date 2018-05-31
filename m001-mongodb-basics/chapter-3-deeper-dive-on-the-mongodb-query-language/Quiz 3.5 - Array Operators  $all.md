# Array Operators: $all

## Problem:
Connect to our class Atlas cluster from the mongo shell or Compass and view the **100YWeatherSmall.data** collection. The **sections** field in this collection identifies supplementary readings available in a given document by a three-character code. How many documents list: "AG1", "MD1", and "OA1" among the codes in their **sections** array. Your count should include all documents that include these three codes regardless of what other codes are also listed.

## Choose the best answer:
* 2000
* 9803
* 10200
* 15442
* 17348

## Answer:
* 10200

## Detailed Answer:
You can find this answer in the mongo shell or in Compass.

In the mongo shell, assuming you've connected to the M001 class Atlas cluster, you can issue the following commands to find this value.

```
use 100YWeatherSmall

db.data.find({sections: {$all: ["AG1", "MD1", "OA1"]}}).count()
```

In Compass, navigate to the **100YWeatherSmall**.data collection and then apply the following filter in either the Schema or Documents view.

```
{sections: {$all: ["AG1", "MD1", "OA1"]}}
```