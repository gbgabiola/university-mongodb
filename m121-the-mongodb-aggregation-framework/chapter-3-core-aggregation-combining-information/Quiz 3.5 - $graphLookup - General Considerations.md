# $graphLookup: General Considerations

## Problem:
Consider the following statement:

```
``$graphLookup`` is required to be the last element on the pipeline.
```

Which of the following is true about the statement?

## Choose the best answer:
1. This is incorrect. **graphLookup** needs to be the first element of the pipeline, regardless of other stages needed to perform the desired query.
2. This is correct because **$graphLookup** pipes out the results of recursive search into a collection, similar to **$out** stage.
3. This is correct because of the recursive nature of **$graphLookup** we want to save resources for last.
4. This is incorrect. **$graphLookup** can be used in any position of the pipeline and acts in the same way as a regular **$lookup**.


## Answer
4. This is incorrect. **$graphLookup** can be used in any position of the pipeline and acts in the same way as a regular **$lookup**.

## Detailed Answer:
