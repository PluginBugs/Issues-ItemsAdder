# HUDs, GUIs...

To see how to use HUDs and GUIs API \(Font Images\) you can check my examples:  
[https://github.com/LoneDev6/GUIExample](https://github.com/LoneDev6/GUIExample)  
[https://github.com/LoneDev6/IAServerMonitor](https://github.com/LoneDev6/IAServerMonitor)

### Access mana bar value example

```java
PlayerHUDsHolderWrapper huds = new PlayerHUDsHolderWrapper(player);
PlayerQuantityHudWapper manaHud = 
                new PlayerQuantityHudWapper(huds, "magiccraft:mana_bar");
manaHud.setFloatValue(2.0f);
```

## FAQ

{% page-ref page="../../plugin-usage/adding-content/font-images/common-errors.md" %}

### Get Emoji or GUI character

```java
new FontImageWrapper("twitteremojis:confirm").getString()
```

