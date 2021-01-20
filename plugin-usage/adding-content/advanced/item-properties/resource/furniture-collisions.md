# Furniture collisions

### How can I make a furniture solid?

You can make a furniture solid adding the "solid" attribute.

```yaml
  table:
    display_name: display-name-table
    permission: table
    lore:
      - 'lore-decorative-item'
    resource:
      material: OAK_WOOD
      generate: false
      model_path: item/table
    behaviours:
      furniture:
        small_hitbox: true
        solid: true
```

![](../../../../../.gitbook/assets/image%20%2815%29.png)

