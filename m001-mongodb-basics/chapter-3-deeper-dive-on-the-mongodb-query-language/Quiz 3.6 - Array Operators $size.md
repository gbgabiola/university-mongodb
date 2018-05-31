# Array Operators: $size

## Problem:
Connect to our class Atlas cluster from the mongo shell or Compass and view the **100YWeatherSmall.data** collection. How many documents in this collection contain exactly two elements in the **sections** array field?

## Choose the best answer:
* 114
* 670
* 2656
* 10700
* 25678

## Answer:
* 2656

## Detailed Answer:
You can find this answer in the mongo shell or in Compass.

In the mongo shell, assuming you've connected to the M001 class Atlas cluster, you can issue the following commands to find this value.

```
use 100YWeatherSmall

db.data.find({sections: {$size: 2}}).count()
```

In Compass, navigate to the **100YWeatherSmall**.data collection and then apply the following filter in either the Schema or Documents view.

```
{sections: {$size: 2}}
```