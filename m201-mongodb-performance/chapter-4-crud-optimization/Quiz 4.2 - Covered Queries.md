# Covered Queries

## Problem:
Given the following indexes:

```
{ _id: 1 }
{ name: 1, dob: 1 }
{ hair: 1, name: 1 }
```

Which of the following queries could be covered by one of the given indexes?

## Check all answers that apply:
1. `db.example.find( { _id : 1117008 }, { _id : 0, name : 1, dob : 1 } )`
2. `db.example.find( { name : { $in : [ "Alfred", "Bruce" ] } }, { name : 1, hair : 1 } )`
3. `db.example.find( { name : { $in : [ "Bart", "Homer" ] } }, {_id : 0, hair : 1, name : 1} )`
4. `db.example.find( { name : { $in : [ "Bart", "Homer" ] } }, {_id : 0, dob : 1, name : 1} )`

## Answer:
4. `db.example.find( { name : { $in : [ "Bart", "Homer" ] } }, {_id : 0, dob : 1, name : 1} )`

## Detailed Answer:
* **db.example.find( { _id : 1117008 }, { _id : 0, name : 1, dob : 1 } )**

No, this query would use the _id index, which doesn't match the projected fields.

* **db.example.find( { name : { $in : [ "Alfred", "Bruce" ] } }, { name : 1, hair : 1 } )**

No, this query would use the { name: 1, dob: 1 } index, but it forgets to omit the _id field.

* **db.example.find( { name : { $in : [ "Bart", "Homer" ] } }, {_id : 0, hair : 1, name : 1} )**

No, this query would use the { name: 1, dob: 1 } index, but it is projecting the hair field.

* **db.example.find( { name : { $in : [ "Bart", "Homer" ] } }, {_id : 0, dob : 1, name : 1} )**

Yes, this query would use the { name: 1, dob: 1 } index, which matches the fields in the projection.