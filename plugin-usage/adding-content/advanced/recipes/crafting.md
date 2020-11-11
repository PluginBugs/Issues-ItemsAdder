---
description: This recipe allows your users to craft an item
---

# Crafting

## Example

```yaml
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
    top_hat:
      permission: itemsadder.top_hat
      enabled: true
      pattern:
      - XWX
      - XWX
      - WWW
      ingredients:
        W: BLACK_WOOL
      result:
        item: itemsadder:top_hat
        amount: 1
```

In this example I created two `crafting_table` recipes called `deadmau5_hat` and `top_hat`

## Special features

```yaml
    peeled_potato:
      permission: itemsadder.peeled_potato
      enabled: true
      pattern:
      - XXX
      - XKP
      - XXX
      ingredients:
        K: itemsadder:knife
        P: POTATO
      result:
        item: itemsadder:peeled_potato
        amount: 1
      return_items:
        decrement_durability:
          knife:
            item: knife
            amount: 1
        play_sound:
          name: itemsadder:item.knife.use
          volume: 1
          pitch: 1
```

For example this is the `peeled_potato` recipe. This is a special recipe which uses a knife as ingredient of  the crafting \(and a potato\) and decrements its durability when player crafts one peeled potato without making it disappear.  


![](../../../../.gitbook/assets/image%20%281%29.png)

As you can see you can also play a sound using `play_sound`

