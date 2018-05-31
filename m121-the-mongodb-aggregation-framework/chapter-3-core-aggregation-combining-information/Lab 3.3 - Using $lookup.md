# Lab 3.3: Using $lookup

## Problem:
Which alliance from **air_alliances** flies the most **routes** with either a Boeing 747 or an Airbus A380 (abbreviated 747 and 380 in **air_routes**)?

## Choose the best answer:
1. "OneWorld"
2. "SkyTeam"
3. "Star Alliance"

## Answer:
2. "SkyTeam"

## Detailed Answer:

```
db.air_routes.aggregate([
	{
		$match: {
            $or: [{ airplane: "380" }, { airplane: "747" }]
        }
	},
    {
		"$lookup": {
			"from": "air_airlines",
			"localField": "airline.name",
			"foreignField": "name",
			"as": "airlines"
		}
    },
	{
        $unwind: '$airlines'
    },
	{
		$group: {
            _id: "$airlines.name",
            count: { $sum: 1 }
        }
	},
	{
		"$lookup": {
			"from": "air_alliances",
			"localField": "_id",
			"foreignField": "airlines",
			"as": "airlines"
      }
	},
	{
        $unwind: '$airlines'
    },
	{
		$group: {
            _id: "$airlines.name",
            count: { $sum: 1 }
        }
	},
	{
		$sort: { "count": -1 }
	},
	{
		$limit: 1
	},
	{
		$project: { _id: 1 }
	}
])
```