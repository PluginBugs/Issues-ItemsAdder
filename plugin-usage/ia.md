# /ia

ia\_gui.yml contains settings about the  `/ia` command GUI.  
It also contains the "all" category which shows every ItemsAdder item.  
  
If you want to create your own category you have to add it to your own .yml file in your namespace.  
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

