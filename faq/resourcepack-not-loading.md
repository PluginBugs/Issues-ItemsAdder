# 📷Resourcepack not loading

#### Resourcepack not loading, I get an error in chat <a id="resourcepack-not-loading-i-get-an-error-in-chat"></a>

* Check if you have another plugin that uses **custom resourcepacks**, if you have please **disable** its **resourcepack** feature or ItemsAdder won't be able to apply the pack correctly \(you can make them compatible if you've a minimum knowledge on how to merge resourcepacks manually, be sure to not replace ItemsAdder files and you're done. The pack folder of ItemsAdder is `resouce_pack`\)
* Make sure you don't have any resourcepack set in the `server.properties` file
* Minecraft limits servers resourcepacks size to 50MB, be sure to compress your textures and your music files before creating the zip file.
* Be sure that your`custom_url`is a **direct** download link to the zip file. If you paste the link on your browser \(Firefox/Chrome\) you must instantly see the download start, if you see a download page with buttons it's wrong. Please upload it on Dropbox, generate the download/share link and change `dl=0` to `raw=1` at the end of link.
* Be sure to follow all [tutorial ](../plugin-usage/resourcepack-hosting/)steps
* Be sure the port is opened if you use self-host.
* Be sure you're **NOT** using my `pack_21521367.zip` file as base for your pack.  You **MUST** use the new generated `pack.zip` file. Read [tutorial here](../plugin-usage/resourcepack-hosting/resourcepack-self-hosting.md)



#### _My players can't see textures! But I've followed the whole tutorial_ <a id="my-players-cant-see-textures-but-ive-followed-the-whole-tutorial"></a>

There are three ways to fix this issue:

* If your players can't see the new items just link them this simple screens to fix it! [http://imgur.com/a/SG0AU](http://imgur.com/a/SG0AU)​
* If you still have problems **delete** the **server** from your **servers list**, add it again and then **enable resource packs**.
* If you still have problems leave the server, go to **%appdata%/.minecraft/server-resource-packs** and **delete everything**. Then join the server again.

{% hint style="danger" %}
Make sure you're not using **UPPERCASE** or **special characters** in items **names**, **namespaces**, **texture** files \(png\) and **model** files \(json\)
{% endhint %}

