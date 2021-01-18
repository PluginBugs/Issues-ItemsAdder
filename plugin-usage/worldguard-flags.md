# WorldGuard flags

## Flags list

### ia-furniture-sit

This flags allows your players to sit on furnitures or not \(furnitures with `furniture_sit` [behaviour](adding-content/advanced/item-properties/behaviours.md)\)

### ia-campfire-item-add

Allow user to move item to campfire

### ia-campfire-item-remove

Allow user to remove item from campfire

### ia-vehicle-sit

Allow user to sit on any vehicle in the region

### ia-vehicle-personal-sit

allow user to sit only on own vehicles in the region

{% hint style="info" %}
Set **ia-vehicle-sit** to Deny and **ia-vehicle-personal-sit** to Allow to let your players only sit on personal vehicles
{% endhint %}

## Common issues

{% hint style="warning" %}
If your users **cannot sit** on **furnitures** even if you set the correct flag:

* check if you are using the `__global__ region` as your main region \(the one on which you applied the furniture flag\). If yes, please create a new region. global region is known to give some issues with some plugins flags.
* check if you set the `build` or `passthrough` flag.  Remember that these flags must not be changed, you should keep the default value \(unselected, gray text\)
{% endhint %}

