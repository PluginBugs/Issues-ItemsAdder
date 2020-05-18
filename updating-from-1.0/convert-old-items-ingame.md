# Convert old items/blocks ingame

{% hint style="danger" %}
**It's recommended to start a fresh new world and don't use the old one as converters work but are experimental.**
{% endhint %}

{% hint style="danger" %}
These features MAY be laggy, leave them enabled only for some days and then disable them to avoid useless lag.
{% endhint %}

## How to auto convert old items in your worlds

When you update from ItemsAdder 1.0 to 2.0 you noticed that most of the items has changed, so they are not the same as old items before the update.  
That's why I had to code a feature that auto replaces old items with new items. This process is run everytime a player opens an inventory in the world \(chests, containers.. but NOT their own inventory\).

In order to enable this you have to set this property to true in `converter.yml` of **ItemsAdder 2.0**

#### Be sure to set inventory-open: true

```text
items-auto-update:
  debug: false
  inventory-open: true
```

## How to auto convert old blocks placed in worlds

You have to open `converter.yml` and map your own old blocks **model\_id** with the new **namespaced** block of IA 2.0. For example I've already added old ItemsAdder 1.0 blocks map to convert them to 2.0 namespaced blocks.

#### Be sure to set enabled: true

```text
blocks:
  enabled: true
  debug: false
  conversion-map:
    "1": "itemsadder:ruby_block"
    "2": "itemsadder:crystal_block"
    "3": "itemsadder:spinel_block"
    "4": "itemsadder:turquoise_block"
    "5": "itemsadder:aqua_aura_block"
    "6": "itemsadder:amethyst_block"
    "7": "itemsadder:amethyst_prism_block"
    "8": "itemsadder:crying_obsidian"
    "9": "itemsadder:nice_stone"
    "10": "itemsadder:nice_wood"
    "11": "itemsadder:modern_stone"
    "12": "itemsadder:modern_sandstone"
    "13": "itemsadder:modern_quartz"
    "14": "itemsadder:ruby_ore"
    "15": "itemsadder:spinel_ore"
    "16": "itemsadder:turquoise_ore"
    "17": "itemsadder:aqua_aura_ore"
    "18": "itemsadder:amethyst_ore"
    "19": "itemsadder:bronze_ore"
    "20": "itemsadder:mysterious_ore"
    "21": "itemsadder:end_ore"
    "22": "itemsadder:restoration_table"
    "23": "itemsadder:customization_table"
    "24": "itemsadder:iron_dirt_ore"
    "25": "itemsadder:gold_dirt_ore"
    "26": "itemsadder:coal_dirt_ore"
    "27": "itemsadder:blaze_powder_ore"
    "28": "itemsadder:nether_alchemy_ore"
```

