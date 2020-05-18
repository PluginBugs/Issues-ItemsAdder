# Blocks

```yaml
specific_properties:
  block:
    placed_model:
      type: REAL
      break_particles: BLOCK
    cancel_drop: true #default is false. if true the custom block won't be dropped when
                      #player mines it
    light_level: 12 #make block emit light
    #tools you can't use to break block(accepts partial name of material/customitem)
    break_tools_blacklist:
    - WOODEN_PICKAXE
    - STONE_PICKAXE
    - IRON_PICKAXE
    #tools you can use to break block(accepts partial name of material/customitem)
    break_tools_whitelist:
    - DIAMOND_PICKAXE
    - PICKAXE
    - pickaxe
```

## placed\_model

this property can have these value:

* `REAL`
  * uses a real block \(mushroom\), no lag, no entities, 100% real blocks.
  * downside: max of **191** blocks in total
* `TILE`
  * uses tile blocks \(modified spawner with custom skin\). It's not an entity but it have some downsides. Good thing is that you can create infinite blocks, there is no amount limit like **REAL** blocks.
  * downsides:
    * not a 100% real block, it's a retextured spawner
    * texture/model vanishes on high distance, so it will reveal the spawner vanilla texture
    * it could cause clientside lag if A LOT of blocks are in the player field of view, but only on lowend PCs.

{% hint style="warning" %}
It's better to use REAL blocks for decorative blocks/ores and use TILE blocks for trade machines and machinery/rare decorative blocks.  
You should not use TILE blocks for ores because it COULD cause a bit of lag on chunk generation.
{% endhint %}

## cancel\_drop

Cancel drop when block is broken.  
Useful if you have any mineral that will drop out of the block \(loots\), to avoid exploits.

{% hint style="info" %}
If you use silk touch enchanted tool to break the block you will still get the block but it won't drop any item from its loot 
{% endhint %}

## Tools blacklist and whitelist

You can set "\_PICKAXE" so every pickaxe will match the list rule, also "\_AXE" as the plugin checks if the material name contains the word you set in the rule.  
It also works for custom items ids, so for example if you set "ruby\_" every ruby tool will work \(ruby\_pickaxe, ruby\_axe...\)

### break\_tools\_blacklist

Blacklist of tools that cannot break this block

### break\_tools\_whitelist

Whitelist of tools that can break this block

