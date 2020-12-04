# I see crisp textures far away!

{% hint style="warning" %}
If you see dotted and not smooth textures in far away it's a common mistake of resourcepacks maker.  
Minecraft has a bug that disables mipmap if you set textures which their size is not a multiple of two
{% endhint %}

![LEFT: without mipmap. RIGHT: with mipmap](../.gitbook/assets/image%20%2819%29.png)

## **How to fix?**

It's easy! Just follow this:

* open your Minecraft GAME log file, **not server** logs \(usually it's in `%appdata%\.minecraft\logs\latest.log` if not please search inside this folder `%appdata%\.minecraft\logs\`\)
* search for this text `limits mip level`
* identify the problematic texture, for example `Texture mcicons:item/icon_toggle_off with size 30x30 limits mip level from 3 to 1`
* Fix the texture. To fix it you have to resize it to a size of: 16x16, 32x32, 128x128, 256x256, you decide one of these.

Done!

