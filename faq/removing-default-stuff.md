# Removing default stuff

## How can I remove all the items and default stuff?

If you only want to make your own items, blocks and other things it's easy!  
Follow this tutorial.  


### 1. Config.yml

Open plugin `config.yml` file and set this to **false**.

```yaml
  extract-default-items: false
  extract-default-resources: false
```

### 2. Delete the folders you don't need. Select from this list.

#### Twitter emojis

`plugins\ItemsAdder\data\items_packs\twitteremojis`  
`plugins\ItemsAdder\data\resource_pack\assets\twitteremojis`

#### Magic craft example

`plugins\ItemsAdder\data\items_packs\magiccraft`  
`plugins\ItemsAdder\data\resource_pack\assets\magiccraft`

#### Minecraft Emojis

`plugins\ItemsAdder\data\items_packs\mcemojis`  
`plugins\ItemsAdder\data\resource_pack\assets\mcemojis`

#### ItemsAdder items

`plugins\ItemsAdder\data\items_packs\mcemojis`  
`plugins\ItemsAdder\data\resource_pack\assets\itemsadder`

####  Example items

`plugins\ItemsAdder\data\items_packs\example`  
`plugins\ItemsAdder\data\resource_pack\assets\example`

{% hint style="danger" %}
## Do not delete other folders which are not listed in the previous list.

If you delete minecraft, mcguis or mcicons folders some parts of the plugin will stop working.
{% endhint %}



