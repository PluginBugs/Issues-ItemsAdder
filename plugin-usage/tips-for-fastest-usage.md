# Conseils pour une utilisation rapide

## It takes too much time editing the pack and uploading it online!

Yes if you do that the wrong way ;\) Read this:

{% hint style="info" %}
It's a good practice to create a **test server on your PC** with:

* [ItemsAdder](https://www.spigotmc.org/resources/%E2%9C%85must-have%E2%9C%85-itemsadder%E2%9C%A8textures-3d-models-emojis-ores-blocks-wings-tails-hats-more.73355/)
* [IALib](https://www.spigotmc.org/resources/ialib.75974/)
* [ProtocolLib](https://www.spigotmc.org/resources/protocollib.1997/)
* [LightAPI Fork](https://www.spigotmc.org/resources/lightapi-fork.48247/)

ItemsAdder with this resourcepack config:

```yaml
resource-pack:
  apply-on-join: true
  kick-player-on-decline: false
  delay-ticks: 1
  self-host:
    enabled: true
    server-ip: '127.0.0.1'
    pack-port: 8163
  external-host:
    enabled: false
    url: 'http://example.dropbox.com'
```

Doing this you'll have a fast and easy to use configuration evironment. You can add items and edit the pack on the fly.

When you edit an item texture/model and you edit its configuration you will use command `/iareload` , `/iazip` and then on your client`/iatexture`, doing this you'll see changes applied at realtime.

So after you finished adding items and configuring them you'll be able to upload everything on your online server, upload your `pack.zip` following the next tutorial down here.
{% endhint %}

{% page-ref page="resourcepack-hosting/resourcepack-on-dropbox.md" %}

{% hint style="warning" %}
It's a good practice to not edit ItemsAdder textures/models directly on your online server.  
Players hate lag on plugins reload, server restarts, having to redownload the pack when they're already player.. keep that in mind.
{% endhint %}

{% hint style="danger" %}
It's a good thing not to edit my custom items as surely in the future they can be edited and you'll go crazy maintaining both your customization and my updates.  
So if you want to edit items just make your own
{% endhint %}

