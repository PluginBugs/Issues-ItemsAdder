# First install

## Video

{% embed url="https://youtu.be/GKGnlF4zZVg" %}

## Step 1

You should do this first configuration on your test server on your PC to avoid mistakes and too many restarts.. players don't like when server is down ;\) You can upload files to your real server after you finished here.

{% hint style="danger" %}
If you already own ItemsAdder old 1.0 version please rename **plugins/ItemsAdder** folder to **ItemsAdder\_backup**
{% endhint %}

* install [**ProtocolLib**](https://www.spigotmc.org/resources/protocollib.1997/)
* install [**IALib**](https://www.spigotmc.org/resources/ialib.75974/)
* install [**LightAPI**](https://www.spigotmc.org/resources/lightapi-fork.48247/)
* put **ItemsAdder.jar** file inside your plugins folder
* start the server
* let ItemsAdder finish loading **everything**
* stop server

## Step 2

* join the server and execute the command `/iazip` when the plugin is fully loaded
* open plugins\ItemsAdder\config.yml
* follow this tutorial:

{% page-ref page="plugin-usage/resourcepack-hosting/resourcepack-self-hosting.md" %}



{% hint style="warning" %}
Remember to use the command `/iazip` each time you want the plugin to update the file `pack.zip`
{% endhint %}

