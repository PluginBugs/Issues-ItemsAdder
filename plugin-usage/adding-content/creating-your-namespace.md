# Création de votre espace de noms

{% hint style="warning" %}
If you don't know what I mean by **namespace** please read [namespace tutorial](basic-concepts/namespace.md)
{% endhint %}

## Creating the items\_packs subfolder

In order to keep everything organized you have to create your own namespace. First step is to create a subfolder inside: `plugins\ItemsAdder\data\items_packs`

So this example **namespace** will be `myitems` so create a folder names like the namespace.

![](../../.gitbook/assets/image%20%289%29.png)

Open the myitems folder and create a new file, you can call it like as prefer, I named it `myswords.yml`

![](../../.gitbook/assets/image%20%2811%29.png)

Open the new **.yml** file and paste this:

```yaml
info:
  namespace: myitems
```

As you see I set **namespace** to `myitems`, which is the **namespace** I chose before and it's the same name of the **folder**. Remember to change it based on your **namespace**.

{% hint style="info" %}
You can create as many **namespaces** you want! This allows you to easly organize your packs of items.
{% endhint %}

{% hint style="info" %}
You can create as many as **.yml** files you want in the same namespace!  
This allows you to organize items/things types better.  
For example I divided my items in swords, blocks, food, drinks...
{% endhint %}

{% hint style="warning" %}
**All this "nesting" could seem boring** **but** **trust me**, it reduces errors as much as possible and allows you to find everything easly.
{% endhint %}

