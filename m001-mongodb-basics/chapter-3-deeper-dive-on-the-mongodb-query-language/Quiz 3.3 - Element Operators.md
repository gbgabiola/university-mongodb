# Element Operators

## Problem:
Connect to our class Atlas cluster from the mongo shell or Compass and answer the following question. How many documents in the **100YWeatherSmall.data** collection do **NOT** contain the key **atmosphericPressureChange**.

## Choose the best answer:
* 1
* 2679
* 10345
* 33989
* 40668

## Answer:
* 40668

## Detailed Answer:
You can find this answer in the mongo shell or in Compass.

In the mongo shell, assuming you've connected to the M001 class Atlas cluster, you can issue the following commands to find this value.

```
use 100YWeatherSmall

db.data.find({atmosphericPressureChange: {$exists: false}}).count()
```

In Compass, navigate to the 100YWeatherSmall.data collection and then apply the following filter in either the Schema or Documents view.

```
{atmosphericPressureChange: {$exists: false}}
```