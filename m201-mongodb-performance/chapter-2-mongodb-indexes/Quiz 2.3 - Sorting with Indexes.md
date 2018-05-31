# Sorting with Indexes

## Problem:
Given the following schema for the **products** collection:

```
{
  "_id": ObjectId,
  "product_name": String,
  "product_id": String
}
```

And the following index on the **products** collection:

```
{ product_id: 1 }
```

Which of the following queries will use the given index to perform the sorting of the returned documents?

## Check all answers that apply:
1. db.products.find({}).sort({ product_id: 1 })
2. db.products.find({}).sort({ product_id: -1 })
3. db.products.find({ product_id: '57d7a1' }).sort({ product_id: -1 })
4. db.products.find({ product_name: 'Soap' }).sort({ product_id: 1 })
5. db.products.find({ product_name: 'Wax' }).sort({ product_name: 1 })

## Answer:
1. db.products.find({}).sort({ product_id: 1 })
2. db.products.find({}).sort({ product_id: -1 })
3. db.products.find({ product_id: '57d7a1' }).sort({ product_id: -1 })
4. db.products.find({ product_name: 'Soap' }).sort({ product_id: 1 })

## Detailed Answer:
* **db.products.find({}).sort({ product_id: 1 })**

Yes.

* **db.products.find({}).sort({ product_id: -1 })**

Yes, in this case the index will be traversed backwards for sorting.

* **db.products.find({ product_id: '57d7a1' }).sort({ product_id: -1 })**

Yes, in this case the index will be used to filter and sort by traversing the index backwards.

* **db.products.find({ product_name: 'Soap' }).sort({ product_id: 1 })**

Yes, in this case the index will be used to first fetch the sorted documents, and then the server will filter on products that match the product name.

* **db.products.find({ product_name: 'Wax' }).sort({ product_name: 1 })**

No, there is no index for sorting or filtering. A collection scan and an in-memory sort will be necessary.