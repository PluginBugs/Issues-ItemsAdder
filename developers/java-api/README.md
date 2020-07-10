# Java API

ItemsAdder includes an easy to use API for Java developers.  
To access it just include **dev.lone.itemsadder.api.ItemsAdder** in your code.

{% hint style="danger" %}
Most of this API down here will be rewritten, I won't delete the old API to maintain backwards compatibility, but keep in mind that you'd probably prefer the new API which will be more modular and easy to use.
{% endhint %}

```java
//check if itemsadder finished loading its items and if they are available
//PLEASE USE ItemsAdderFirstLoadEvent INSTEAD
public static boolean areItemsLoaded()

//Checks if an item is a custom item made with ItemsAdder
public static boolean isCustomItem(ItemStack itemStack)
public static boolean isCustomItem(String customItemName)

//Get an ItemsAdder custom item by its name in config
public static ItemStack getCustomItem(String nameInConfig)

//Spawns a block made with ItemsAdder specifying the itemstack 
//(obtain it with getCustomItem)
public static void placeCustomBlock(Location location, ItemStack customBlock)
public static void placeCustomBlock(Location location, ItemStack customBlock, boolean lightweight)

//get custom block loots
public static List<ItemStack> getCustomBlockLoot(Block block, ItemStack tool, boolean includeSelfBlock)

//Check if a block in the world is a custom block made with ItemsAdder
public static boolean isCustomBlock(Block block)

//plants custom seed like a normal player would do
public static void placeCustomCrop(Location location, ItemStack seed)

//check if block is custom planted crop with custom seed
public static boolean isCustomCrop(Block block)

//get custom seed of custom crop
public static String getCustomSeedNameFromCrop(Block block)

//returns the ItemStack of a custom block in world
public static ItemStack getCustomBlock(Block block)

//check if an entity in world is a furniture
public static boolean isFurniture(Entity entity)

//check if an ItemStack is a specific custom item 
//(example: check if a pickaxe is 'amethyst_pickaxe')
public static boolean matchCustomItemName(ItemStack itemStack, String customItemName)

//get name of the item in config (ex: 'ruby_pickaxe')
public static String getCustomItemName(ItemStack itemStack)

//get name of config where the item is declared (ex: 'items/swords')
public static String getCustomItemFileName(ItemStack itemStack)

//gets usages remaining of this item (-999 if it has no usages specified = infinite)
public static int getCustomItemUsages(ItemStack itemStack)

//set custom item durability (also works with vanilla items and with
//custom items with default vanilla durability)
public static ItemStack setCustomItemDurability(ItemStack item, int durability)

//get custom durability
public static int getCustomItemDurability(ItemStack itemStack)

//get max custom durability 
public static int getCustomItemMaxDurability(ItemStack itemStack)
```

