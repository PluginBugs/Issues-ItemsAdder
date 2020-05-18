# Actions

## What are actions?

Actions are what will happen when an event is triggered.

### List of actions:

* play\_sound
* stop\_sound
* execute\_commands
* play\_particle
* play\_effect
* increment\_durability
* decrement\_durability
* decrement\_usages
* increment\_amount
* decrement\_amount
* drop\_exp
* feed
* replace\_properties
* give\_item
* replace\_near\_blocks
* glow\_near\_blocks
* multiple\_break
* potion\_effect
* remove\_potion\_effect
* explosion
* increment\_player\_stat
* decrement\_player\_stat
* cancel

{% hint style="info" %}
You can set the same action multiple times. You just have to add `_anything` at the end.  
For example if you want to play two sounds you have to write this:

```yaml
play_sound_first:
  name: itemsadder:ambient.creepy
  volume: 1
  pitch: 1
play_sound_second:
  name: minecraft:ambient.cave
  volume: 1
  pitch: 1
```
{% endhint %}

```yaml
play_sound:
  name: itemsadder:ambient.creepy
  volume: 1
  pitch: 1
  
  
stop_sound:
  name: "itemsadder:music_disc.cdk_sunday"
  
  
execute_commands:
  first_example:
    command: 'tellraw {player} {"text":"wow you did something!","color":"gold"}'
    as_console: true
  second:
    command: 'help'
    as_console: false
  third:
    command: 'give {player} diamond'
    as_console: true
    
    
play_particle:
  name: "ENCHANTMENT_TABLE"
  
  
play_effect:
  name: SMOKE
  
increment_durability:
  amount: 10
  
  
decrement_durability:
  amount: 10
  
  
decrement_usages:
  amount: 1


increment_amount:
  amount: 1
          
          
decrement_amount:
  amount: 1    


drop_exp:
  chance: 50
  min_amount: 1
  max_amount: 3
    

feed:
  amount: 6
    
# Replaced properties of the current item copying them from another.
# For now you can only do that with custom_model_data. More will be added.
replace_properties:
  custom_model_data:
    copy_from_item: "itemsadder:closed_lightsaber"
    restorable: true


give_item:
  item: empty_cup
  amount: 1
  
# Replaces blocks around the block you interacted with or break
replace_near_blocks:
  radius:
    x: 2
    y: 2
    z: 2
  from: LAVA
  to: OBSIDIAN
  decrement_durability: 8
  no_physics: false #default is false
  
# Glows blocks around the block you interacted with or break
glow_near_blocks:
  decrement_durability:
    amount: 1
  radius:
    x: 50
    y: 50
    z: 50
  material: DIAMOND_ORE
  
# Breaks multiple blocks around the block you interacted with or break
multiple_break:
  keep_ores: true
  drop_all_blocks:
    enabled: true
    need_silk_touch: true
  size: 3
  depth: 3
  
  
potion_effect:
  type: UNLUCK
  duration: 100
  amplifier: 0


remove_potion_effect:
  type: GLOWING
  
  
explosion:
  power: 2
  fire: true
  break_blocks: true
  
# Special action that allows you to increment player stat linked to an hud
#in this case hud named: "itemsadder:mana_bar"
increment_player_stat:
  name: "itemsadder:mana_bar"
  amount: 1
  
# Special action that allows you to decrement player stat linked to an hud
#in this case hud named: "itemsadder:mana_bar"
decrement_player_stat:
  name: "itemsadder:mana_bar"
  amount: 1
  
# Special action to make the event cancelled (the event that called this action)
cancel: true
```

### 

