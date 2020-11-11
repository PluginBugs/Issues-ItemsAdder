---
description: This recipes allows your users to cook/smelt materials
---

# Cooking

## Example

```yaml
  cooking:
    cooked_sausage:
      permission: itemsadder.cooked_sausage
      ingredient:
        item: itemsadder:sausage
      machines:
      - FURNACE
      - BLAST_FURNACE
      exp: 1
      cook_time: 200
      result:
        item: itemsadder:cooked_sausage
        amount: 1
```

In this example I created a`cooking` recipe called `cooked_sausage`

`machines` is the list of vanilla machines that can smelt/cook the item  
`exp` is the exp earned by the player when cooking is completed  
`cook_time` is the time needed to complete the cooking process \(**in ticks**\)

