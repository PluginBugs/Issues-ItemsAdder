# Armor textures

If you want to add a custom texture and not just a custom color to armors you can use Optifine.

### Example custom textured armor

![](../../../.gitbook/assets/image%20%2823%29.png)

![](../../../.gitbook/assets/image%20%2825%29.png)

### Step 1

Create your **custom namespace** \(if you didn't already\), follow[ this tutorial](../beginners/creating-your-namespace.md).  
In this tutorial **my namespace** is named `mystuff`

### Step 2

Create **custom textures** for the **inventory items**. I put them in ****the **folder** `plugins\ItemsAdder\data\resource_pack\assets\mystuff\textures\item\example_1`

![](../../../.gitbook/assets/image%20%2821%29.png)

### Step 3

Create **custom textures** for **worn armor** \(when user wears it\). You can get a **template** from here:  
`plugins\ItemsAdder\data\resource_pack\assets\minecraft\textures\models\armor\leather_layer_1.png`  
`plugins\ItemsAdder\data\resource_pack\assets\minecraft\textures\models\armor\leather_layer_2.png`

**Edit** the **textures** as you wish \(use Paint.NET, Photoshop, GIMP or similar programs\) and **save** them as `layer_1.png` and `layer_2.png` 

### Step 4

Create the `optifine` folder, this is where we want to put out **custom textures** for the **worn armor**: `plugins\ItemsAdder\data\resource_pack\assets\minecraft\optifine`

{% hint style="warning" %}
You **must create** it under the folder `minecraft`, sadly you **cannot** create the `optifine` folder inside your **namespace** folder \(in this case `mystuff`\), it's an **optifine limitation**.
{% endhint %}

### Step 5

Now save the **previously created** worn textures \(`layer_1.png` and `layer_2.png` \) inside this folder: `plugins\ItemsAdder\data\resource_pack\assets\minecraft\optifine\cit\mystuff\armors\example_1\entity`

So you have this:

![](../../../.gitbook/assets/image%20%2824%29.png)

### Step 6

**Create** these files: **boots.properties**, **chestplate.properties**, **helmet.properties**, **leggings.properties** inside `plugins\ItemsAdder\data\resource_pack\assets\minecraft\optifine\cit\mystuff\armors\example_1\entity`

Each of the files must contain this:

```elixir
nbt.itemsadder.namespace=mystuff
nbt.itemsadder.id=example_chestplate_1

type=armor
items=diamond_chestplate
texture.diamond_layer_1=layer_1
texture.diamond_layer_2=layer_2
```

For each of the `.properties` files you have to **change** the **1th** line setting **your namespace** instead of "mystuff", the **2nd line** to your **item id** and the **5th line** to the **item type** \(`diamond_leggings` , `diamond_boots` ....\)

### Step 7

**Create** a **file** to contain this custom armor, to better organize it. Name it **example\_1.yml** and **place it** inside your namespace, in this example: `plugins\ItemsAdder\data\items_packs\mystuff\example_1.yml`

### Step 8

**Add content** to the **yml file**. As you can see I decided to base my items on the Minecraft DIAMOND armor and I didn't specify any color because I don't need to color it, Optifine will apply a texture to it.

```yaml
info:
  namespace: mystuff
items:
  example_helmet_1:
    display_name: Example
    permission: example_helmet_1
    resource:
      generate: true
      material: DIAMOND_HELMET
      textures:
      - item/example_1/helmet.png
    durability:
      max_custom_durability: 275
    specific_properties:
      armor:
        slot: head
    attribute_modifiers:
      head:
        armor: 9
        armorToughness: 1
  example_chestplate_1:
    display_name: Example
    permission: example_chestplate_1
    resource:
      generate: true
      material: DIAMOND_CHESTPLATE
      textures:
      - item/example_1/chestplate.png
    durability:
      max_custom_durability: 400
    specific_properties:
      armor:
        slot: chest
    attribute_modifiers:
      chest:
        armor: 7
        armorToughness: 1
  example_leggings_1:
    display_name: Example
    permission: example_leggings_1
    resource:
      generate: true
      material: DIAMOND_LEGGINGS
      textures:
      - item/example_1/leggings.png
    durability:
      max_custom_durability: 375
    specific_properties:
      armor:
        slot: legs
    attribute_modifiers:
      legs:
        armor: 5
        armorToughness: 1
  example_boots_1:
    display_name: Example
    permission: example_boots_1
    resource:
      generate: true
      material: DIAMOND_BOOTS
      textures:
      - item/example_1/boots.png
    durability:
      max_custom_durability: 325
    specific_properties:
      armor:
        slot: feet
    attribute_modifiers:
      feet:
        armor: 3
        armorToughness: 1
```

### Done!

## Notes:

{% hint style="warning" %}
If you will **create another namespace** which contains **other armors** it's **highly adviced** to **maintain** the **same structure** as I did in the tutorial to **avoid mistakes**.

  
For example if you create a new namespace names `space_armors` you will have this **optifine** folder: `plugins\ItemsAdder\data\resource_pack\assets\minecraft\optifine\cit\space_armors\armors`
{% endhint %}

