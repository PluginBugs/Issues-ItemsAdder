# Leaves and transparent blocks problems

{% hint style="danger" %}
### Tree blocks sometimes disappear and become air blocks

This is a know issue in CREATIVE mode as the client doesn't send some packets to the server.  
Please try in survival mode.
{% endhint %}

{% hint style="danger" %}
### REAL\_TRANSPARENT blocks are dropped when water flows on them

I know this bug and I can't fix it without making your server an oven.  
  
Details:  
As you already know Minecraft is not that great and most of the cool features require a lot of hacks to be implemented.  
One of these are custom blocks. To fix this water bug I'd have to listen to the water flowing event and check if every block around the water is a custom block. This event is called a looooooot of times in midsized server and I can't make the plugin lag everything.
{% endhint %}

