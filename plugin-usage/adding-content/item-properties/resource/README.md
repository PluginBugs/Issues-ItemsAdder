---
description: Properties that allows customization of item graphics
---

# Resource

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

## Use your own custom model

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

## Important note

{% hint style="warning" %}
If your custom 3D model .json is using a custom texture .png and not textures already included in Minecraft you have to add your [namespace ](../../basic-concepts/namespace.md)to the texture, let me make an example:

Your original texture \(**wrong**\):

```javascript
"textures": {
    "texture": "items/my_texture"
},
```

The **correct** usage:

```javascript
"textures": {
    "texture": "YOUR_NAMESPACE:items/my_texture"
},
```

\(`YOUR_NAMESPACE` is the **name** of **your namespace**, obviously\)
{% endhint %}

## Transparent textures \(glass and similar\)

{% page-ref page="../../../../faq/can-i-create-slabs-stairs/transparent-textures.md" %}

