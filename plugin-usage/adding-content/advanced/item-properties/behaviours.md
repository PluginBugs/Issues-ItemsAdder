# Behaviours

## What are behaviours?

Behaviours are an **already coded** set of **actions** the item will do and which are **not vanilla**.  
These **behaviours** are already included in the plugin and will allow you to add some already coded functionality to your item.

### List of behaviours included in the plugin

* block\_trade\_machine
* furniture\_trade\_machine
* furniture
* furniture\_sit
* gun
* hat
* music\_disc
* vehicle

```yaml
# This behaviour allows you to open a trade GUI with the following items
# For example black_fishing_rod and red_fishing_rod
block_trade_machine:
  title: "Your title"
  permission: "mypermission.trade.example" # <--- this is optional
  gui_texture: ###THIS IS OPTIONAL, use it only to retexture the GUI
    left: customization_table_left
    right: customization_table_right
  trades_list:
    black_fishing_rod:
      ingredients:
        slot1:
          item: FISHING_ROD
          amount: 1
        slot2:
          item: BLACK_DYE
          amount: 1
      result:
        item: black_fishing_rod
        amount: 1
    red_fishing_rod:
      ingredients:
        slot1:
          item: FISHING_ROD
          amount: 1
        slot2:
          item: RED_DYE
          amount: 1
      result:
        item: red_fishing_rod
        amount: 1
        
furniture_trade_machine:
....... it's the same as block_trade_machine

   
# When you rightclick with that item it will be placed on the ground with an
# armorstand. The armorstand will have the item as helmet and will be invisible.
furniture:
  small_hitbox: true
  gravity: true
  fixed_rotation: false
  light_level: 7  
  solid: false
  opposite_direction: false #makes the model rotate 180 when placed


# If you add this behaviour and "furniture" behaviour you will be able to sit
# on the furniture at the defined height.
furniture_sit:
  sit_height: 0.9
  opposite_direction: true #default is true
  

# Allows you to use this item as a gun. You can decide which projectile must
# be hold on left hand in order to shot.
gun:
  projectile: itemsadder:clip
  

# Allows you to use the current item as hat (same vanilla helmet behaviour)
hat: true


# Allows you to use the current item as a vanilla music disc.
# Remember that you will have to create a custom sound to be able
# to play something.
music_disc:
  song:
    name: "itemsadder:music_disc.cdk_sunday"
    description: "Cdk - Sunday"
    

# Allows you to use the current item as a ridable vehicle
vehicle:
  fixed_rotation: false
  small_hitbox: true
  sit_height: 0
  step_height: 0.1
  size:
    x: 2
    y: 1.7
    z: 1
  speed:
    drive: 1
    jump: 0.3
    fly: 0
  fuel:
    start: 150
    max: 300
    items:
      COAL: 1
      CHARCOAL: 1
      COAL_BLOCK: 9
      "itemsadder:banana": 1
```







