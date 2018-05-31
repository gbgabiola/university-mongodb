# Logical Operators

## Problem:
Connect to our class Atlas cluster from the mongo shell or Compass and view the **ships.shipwrecks** collection. In this collection, **watlev** describes the water level at the shipwreck site and **depth** describes how far below sea level the ship rests. How many documents in the **ships.shipwrecks** collection match either of the following criteria: **watlev** equal to "always dry" or **depth** equal to 0.

## Choose the best answer:
* 501
* 1644
* 2000
* 2331
* 3105

## Answer:
* 2331

## Detailed Answer:
You can find this answer in the mongo shell or in Compass.

In the mongo shell, assuming you've connected to the M001 class Atlas cluster, you can issue the following commands to find this value.

```
use ships

db.shipwrecks.find({$or: [{depth: 0}, {watlev: "always dry"}]}).count()
```

In Compass, navigate to the **ships.shipwrecks** collection and then apply the following filter in either the Schema or Documents view.

```
{$or: [{depth: 0}, {watlev: "always dry"}]}
```