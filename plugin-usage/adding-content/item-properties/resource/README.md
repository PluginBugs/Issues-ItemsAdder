---
description: Properties that allows customization of item graphics
---

# Resource

{% hint style="danger" %}
Make sure you're not using UPPERCASE or special characters in items names, namespaces, texture files \(png\) and model files \(json\)
{% endhint %}

## Automatic generation

In order to tell ItemsAdder which texture/model use for an item you have to add the `resource` attribute.  
This is an example:

```yaml
  resource:
    material: DIAMOND_SWORD
    generate: true
    textures:
    - item/example_item.png
```

`material` is the vanilla material this item will use as base.

`generate` tells to IA if it needs to generate the item model automatically based on textures you listed

`textures` is the list of textures IA will use to generate the model automatically.

### Where do I put textures?

Textures you listed in the `textures` attribute must be placed in the right folder.  
So if you set `textures` like in the example and your **namespace** \(is for example\) `myitems` you will have to put `example_item.png` ****file inside this folder: `plugins\ItemsAdder\data\resource_pack\assets\myitems\textures\item`

If the path doesn't exists create all the folders needed.

{% hint style="info" %}
You can avoid setting `.png` in the `textures` attribute, IA will recognize the file automatically
{% endhint %}

## Use your own 3D custom model \(.json file\)

If you have a custom modelled sword or item you can tell IA not to generate the model automatically.  
This is an example:

```yaml
  resource:
    material: DIAMOND_SWORD
    generate: false
    model_path: item/floating_sword

```

### Where do I put my model?

Model you set in the `model_path`attribute must be placed in the right folder.  
So if you set `model_path` like in the example and your **namespace** \(is for example\) `myitems` you will have to put `floating_sword.json` ****file inside this folder: `plugins\ItemsAdder\data\resource_pack\assets\myitems\models\item`

If the path doesn't exists create all the folders needed.

{% hint style="warning" %}
### My textures are not working!

If your custom model textures are not showing you have to open your model file and fix the textures path.  
For example if you had this:

```yaml
  {
  "textures": {
    "4": "item/alchemy_candles/white_candle",
    "6": "item/alchemy_candles/candle_top",
    "7": "item/alchemy_candles/red_candle",
    "8": "item/alchemy_candles/fire"
  },
```

You have to change it to this \(`your_namespace` is your [namespace ](../../basic-concepts/namespace.md)folder\):

```yaml
{
  "textures": {
    "4": "your_namespace:item/alchemy_candles/white_candle",
    "6": "your_namespace:item/alchemy_candles/candle_top",
    "7": "your_namespace:item/alchemy_candles/red_candle",
    "8": "your_namespace:item/alchemy_candles/fire"
  },
```
{% endhint %}

## Transparent textures \(glass and similar\)

{% page-ref page="../../../../faq/can-i-create-slabs-stairs/transparent-textures.md" %}

## Manually specify custom\_model\_data

If you want to force the usage of a defined custom\_model\_data \(CustomModelData\) you can:

```yaml
    resource:
      material: CLOCK
      model_id: 4000
      generate: false
      model_path: "item/multimeter"
```

You also have to create the model file names "multimeter" \(in this example\) inside this folder: `assets\YOUR_NAMESPACE\models\item`

You can also tell IA to automatically generate the model based on the texture:

```yaml
info:
  namespace: slimefun
items:
  carbonado:
    resource:
      material: PLAYER_HEAD
      generate: true
      model_id: 4000
      textures:
      - slimefun/carbonado.png
```

\`\`

