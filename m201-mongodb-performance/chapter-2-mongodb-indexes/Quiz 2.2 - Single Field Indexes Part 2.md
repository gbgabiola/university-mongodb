# Single Field Indexes Part 2

## Problem:
Which of the following queries can use an index on the **zip** field?

## Check all answers that apply:
1. db.addresses.find( { zip : 55555 } )
2. db.addresses.find( { city : "Newark", state : "NJ" } )
3. db.addresses.find()

## Answer:
1. db.addresses.find( { zip : 55555 } )

## Detailed Answer:
The only one that specifies a zip code, **db.addresses.find( { zip : 55555 } )**, is correct.

The others do not specify a zip code, and so they will not use the index.