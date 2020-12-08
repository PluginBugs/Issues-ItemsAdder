# Worlds populators

### Example: 2 populators

```yaml
worlds_populators:
  custom_block:
    block: myitems:custom_block
    worlds:
    - world
    replaceable_blocks:
    - STONE
    - DIRT
    - ANDESITE
    - GRANITE
    - COBBLESTONE
    - GRAVEL
    biomes:
    - PLAINS
    chance: 70.0
    max_height: 45
    min_height: 25
    amount: 6
    iterations: 1
  custom_block_2:
    block: myitems:custom_block_2
    worlds:
    - world
    replaceable_blocks:
    - DIRT
    chance: 100.0
    max_height: 64
    min_height: 40
    amount: 3
    iterations: 1
```

This code allows you to tell ItemsAdder to generate the block "myitems:custom\_block" in the world named "world" and replace only block of types STONE, DIRT, ANDESITE, GRANITE, COBBLESTONE, GRAVEL and only in biome PLAINS.

### amount, iterations, chance

{% hint style="warning" %}
I suggest you to copy values from the blocks.yml file I created in the itemsadder folder.  
Don't put too high values or the server will lag/crash.  
Take my values as example.  
  
The only thing that you can increase safely as you wish is the **chance**.
{% endhint %}

**iterations**: number of veins to be spawned to make a bigger ore vein  
**amount**: number of blocks in each ore vein \(or the **vein size**\)  
**chance**: chance of that generation to happen in a chunk, you should set it to 100 to normal ores and lower it down for more rare ores.

### Biomes

You can remove this option and the plugin will spawn ores in every biome.

```yaml
  custom_block:
    block: myitems:custom_block
    worlds:
    - world
    replaceable_blocks:
    - STONE
    - DIRT
    - ANDESITE
    - GRANITE
    - COBBLESTONE
    - GRAVEL
    chance: 70.0
    max_height: 45
    min_height: 25
    amount: 6
    iterations: 1
```

### Replaceable blocks

You can remove this option and the plugin will spawn ores replacing every block instead of checking if it can be replaced.

```yaml
  custom_block:
    block: myitems:custom_block
    worlds:
    - world
    chance: 70.0
    max_height: 45
    min_height: 25
    amount: 6
    iterations: 1
```



