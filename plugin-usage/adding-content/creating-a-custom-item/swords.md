# Swords

{% hint style="danger" %}
If you didn't create your namespace please follow the [namespace tutorial](../creating-your-namespace.md).
{% endhint %}

## My first sword

This is an example sword \(remember to change myitems namespace to the one you want\)

```yaml
info:
  namespace: myitems
items:
  mysword:
    display_name: My Sword
    permission: mysword
    resource:
      material: DIAMOND_SWORD
      generate: true
      textures:
      - item/example_item.png
    durability:
      max_custom_durability: 1324
  
```

### Setting the texture

{% page-ref page="../item-properties/resource/" %}



