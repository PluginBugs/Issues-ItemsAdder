# Using MythicMobs

## How to make MythicMobs handle my custom mob

If you want to make MythicMobs handle your custom mob to have more advanced features and control it's really easy!

For example I have this MythicMobs configuration:

```yaml
StaticallyChargedSheep:
  Type: SHEEP
  Display: '&aStatically Charged Sheep'
  Health: 100
  Damage: 2
  Options:
    MovementSpeed: 0.3
  DamageModifiers:
  - LIGHTNING 0
  - FIRE 0.5
  Skills:
  - lightning @LivingInRadius{r=10} ~onTimer:100
```

  
Open your ItemsAdder .yml file where you created the mob and to edit the **replace rule** like this:

```yaml
        replace_mobs_spawn:
          mob1:
            replace_mythicmob:
              name: StaticallyChargedSheep
              always: true
            type: SHEEP
```

{% hint style="warning" %}
It's important to set **replace\_mythicmob** `name` property to your **mythicmob name**.
{% endhint %}

### Random chance

If you want to replace the mythic mob only sometimes \(this allows you to create more skin variations for the name mythicmob\) you just have to set `always: false` and set your spawn rules.  
Example:

```yaml
    replace_mobs_spawn:
      mob1:
        replace_mythicmob:
          name: StaticallyChargedSheep
          always: false
        type: SHEEP
        reason: CUSTOM
        chance: 20
        max_sky_light: 0
        time:
          start: MIDNIGHT
```

{% hint style="warning" %}
Remember to set `reason: CUSTOM` or it won't work as MythicMobs sets the spawn reson to `CUSTOM` and not `NATURAL`.
{% endhint %}



