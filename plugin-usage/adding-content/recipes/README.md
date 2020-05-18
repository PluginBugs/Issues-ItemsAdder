# Recipes

In order to create a recipe for your items in your [namespace ](../basic-concepts/namespace.md)you have to create a special section in one of your .yml files \(or on each one, you decide how you want to organize the plugin\).

## Example

```yaml
info:
  namespace: myitems
recipes:
  crafting_table:
    deadmau5_hat:
      permission: myitems.deadmau5_hat
      enabled: true
      pattern:
      - BXB
      - XBX
      - XXX
      ingredients:
        B: LIGHT_BLUE_WOOL
      result:
        item: myitems:deadmau5_hat
        amount: 1
```

As you can see I created the recipes section in the .yml file, this section can contain each type of recipe.  
In this example I created a `crafting_table` recipe called `deadmau5_hat`

