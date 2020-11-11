# ItemsAdder internal

## Creating your fist mob

You have to create a .yml file in your [namespace ](../../beginners/basic-concepts/namespace.md)folder \(check [other tutorials ](../../beginners/creating-your-namespace.md)for more info\).

{% hint style="info" %}
Consider using the[ official online tool](../../../../files-editor.md) to edit ItemsAdder files. It makes you life easier as it has autocomplete \(press CRTL+SPACE\) which helps you on avoiding mistakes.
{% endhint %}

This is an example for a custom mob names Soul.  
As you can see I set it up like a normal item, but with a special [behaviour ](../item-properties/behaviours.md)named **mob**.

```yaml
info:
  namespace: creaturesplus
items:
  soul:
    display_name: Soul
    permission: creaturesplus
    click_in_ia_gui: false
    resource:
      generate: false
      model_path: "mob/soul/soul"
    behaviours:
      mob:
        ai: HUSK
        hit_color: ff7e7e
        max_health: 40
        y_offset: 0
        lock_head_rotation:
          y: 0
        animation:
          attack: soul_attack
          walk: soul_walking
        replace_mobs_spawn:
          mob1:
            type: ZOMBIE
            reason: NATURAL
            chance: 20
            max_sky_light: 0
            time:
              start: MIDNIGHT
```

This behaviour tells ItemsAdder to replace any naturally spawned `ZOMBIE`with 20% `chance`, at `MIDNIGHT` and only in caves \(`max_sky_light: 0`\).  
The mob will also have head rotation locked \(only on Y axis\), this will avoid it from looking stupid while looking at player when is at an higher position.

`hit_color` is the color the mob will have when damaged by player.   
You can get a valid color from these websites:  
[https://hub.spigotmc.org/javadocs/bukkit/org/bukkit/Color.html](https://hub.spigotmc.org/javadocs/bukkit/org/bukkit/Color.html)  
[https://minecraftcommand.science/armor-color](https://minecraftcommand.science/armor-color)  
[https://misode.github.io/worldgen/biome/](https://misode.github.io/worldgen/biome/) \(use one of the color pickers and copy the value from the right\)

{% hint style="info" %}
Note: I **skipped** the `material` property of `resource` because **it's not needed** for **mobs**, ItemsAdder will automatically handle it.
{% endhint %}

### Animations

You probably noticed that there are two other attributes: `attack` and `walk` **animations**.  
These are infact other items you have to create like this:

```yaml
  soul_walking:
    display_name: soul_walking
    permission: creaturesplus
    show_in_ia_gui: false
    resource:
      generate: false
      model_path: "mob/soul/walking"
    behaviours:
      mob_animation: true
  soul_attack:
    display_name: soul_attack
    permission: creaturesplus
    show_in_ia_gui: false
    resource:
      generate: false
      model_path: "mob/soul/attack"
    behaviours:
      mob_animation: true
```

## Final result

```yaml
info:
  namespace: creaturesplus
items:
  soul:
    display_name: Soul
    permission: creaturesplus
    click_in_ia_gui: false
    resource:
      generate: false
      model_path: "mob/soul/soul"
    behaviours:
      mob:
        ai: HUSK
        hit_color: ff7e7e
        max_health: 40
        lock_head_rotation:
          y: 0
        animation:
          attack: soul_attack
          walk: soul_walking
        replace_mobs_spawn:
          mob1:
            type: ZOMBIE
            reason: NATURAL
            chance: 20
            max_sky_light: 0
            time:
              start: MIDNIGHT
  soul_walking:
    display_name: soul_walking
    permission: creaturesplus
    show_in_ia_gui: false
    resource:
      generate: false
      model_path: "mob/soul/walking"
    behaviours:
      mob_animation: true
  soul_attack:
    display_name: soul_attack
    permission: creaturesplus
    show_in_ia_gui: false
    resource:
      generate: false
      model_path: "mob/soul/attack"
    behaviours:
      mob_animation: true
```

![](../../../../.gitbook/assets/image%20%2816%29.png)

## Spawn the mob naturally

To spawn the mob naturally you have to setup the `replace_mobs_spawn` property.

```yaml
  soul:
    display_name: Soul
    permission: creaturesplus
    click_in_ia_gui: false
    resource:
      generate: false
      model_path: "mob/soul/soul"
    behaviours:
      mob:
        ai: HUSK
        hit_color: ff7e7e
        max_health: 40
        lock_head_rotation:
          y: 0
        animation:
          attack: soul_attack
          walk: soul_walking
        replace_mobs_spawn:
          mob1:
            type: ZOMBIE
            reason: NATURAL
            chance: 20
            max_sky_light: 0
            time:
              start: MIDNIGHT
```

You can create as much as replace rules as you want, for example if you want to replace both `ZOMBIE` and `SKELETON` you can create a second rule

```yaml
        replace_mobs_spawn:
          rule1:
            type: ZOMBIE
            reason: NATURAL
            chance: 20
            max_sky_light: 0
            time:
              start: MIDNIGHT
          rule2:
            type: SKELETON
            reason: NATURAL
            chance: 50
            max_sky_light: 0
            time:
              start: NOON
```

You can decide if to **replace** the mob **or** to **spawn** the custom **mob without replacing** the **original** one.  
You have to use the `spawn_another` property.

```yaml
          rule3:
            type: ZOMBIE
            spawn_another: true
            reason: NATURAL
            chance: 10
            max_sky_light: 0
            time:
              start: MIDNIGHT
```

