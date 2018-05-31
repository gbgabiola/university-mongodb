# Multikey Indexes

## Problem:
Given the following index:

```
{ name: 1 emails: 1 }
```

How many index keys will the following document create?

```
{
  "name": "Beatrice McBride",
  "age": 26,
  "emails": [
      "puovvid@wamaw.kp",
      "todujufo@zoehed.mh",
      "fakmir@cebfirvot.pm"
  ]
}
```

## Check all answers that apply:
* 1
* 2
* 3
* 4

## Answer:
* 3

## Detailed Answer:
Three is the correct answer. There would be the following index keys:

```
"Beatrice McBride", "puovvid@wamaw.kp"
"Beatrice McBride", "todujufo@zoehed.mh"
"Beatrice McBride", "fakmir@cebfirvot.pm"
```