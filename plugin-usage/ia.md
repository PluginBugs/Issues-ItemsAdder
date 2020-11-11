# Editing /ia menu

## Menu settings and "All" category

ia\_gui.yml contains settings about the  `/ia` command GUI.  
It also contains the "all" category which shows every ItemsAdder item.

{% hint style="info" %}
Default categories are inside: `plugins\ItemsAdder\data\items_packs\various_configs\ia_gui_default_categories.yml`
{% endhint %}

## Creating a custom category

If you want to create your own category you have to add it to your own .yml file in your [namespace](adding-content/beginners/basic-concepts/namespace.md).  
This is an example:

```yaml
info:
  namespace: your_namespace
categories:
  armors:
    enabled: true
    icon: "itemsadder:ruby_head"
    name: 'Armors'
    permission: "ia.menu.armors"
    items:
      - "itemsadder:ruby_sword"
      - "itemsadder:ruby_head"
      - "itemsadder:ruby_chest"
      - "itemsadder:ruby_legs"
      - "itemsadder:ruby_boots"
      - "itemsadder:spinel_head"
      - "itemsadder:spinel_chest"
      - "itemsadder:spinel_legs"
```

Remember to give your users permission for each category if you want them to see the categories.  
For example a permission is: **ia.menu.armors**

{% hint style="success" %}
**Categories** with the **same name** and different namespace **will be merged**, this is **helful** if you have two "swords" categories. This allows you to open **/ia** menu and see all swords organized in the same category instead of having 2 swords categories.
{% endhint %}

