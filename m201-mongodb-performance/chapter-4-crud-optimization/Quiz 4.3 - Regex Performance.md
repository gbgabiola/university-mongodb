# Regex Performance

## Problem:
Given the following indexes:

```
> db.products.createIndex({ productName: 1 })

```

And the following query:

```
> db.products.find({ productName: /^Craftsman/ })
```

Which of the following are true?

## Check all answers that apply:
1. The query will need to do a collection scan.
2. The query will do an index scan.
3. The query will likely need to look at all index keys.
4. The query would match a productName of "Screwdriver - Craftsman Brand"

## Answer:
2. The query will do an index scan.

## Detailed Answer:
* **The query will need to do a collection scan.**

No, there is an index on productName.

* **The query will do an index scan.**

Yes, there is an index on productName.

* **The query will likely need to look at all index keys.**

No, the use of the caret at the beginning reduces the number of keys examined.

* **The query would match a productName of "Screwdriver - Craftsman Brand"**

No, the query only matches strings that begin with "Craftsman".