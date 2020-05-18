# Resourcepack self hosting

With ItemsAdder 2.0 you can host the resourcepack directly on your server!   
No need to pay for a website host and **no need to upload the pack everytime you make a change!**

{% hint style="warning" %}
Your hosting service must let you get additional ports for your server.  
If your hosting service doesn't provide you additional ports you have to use DropBox, check this tutorial:
{% endhint %}

{% page-ref page="resourcepack-on-dropbox.md" %}

## But I don't want/can't open another port on the server

{% hint style="info" %}
If you don't want to host the pack on your server you can just configure `config.yml` following the next tutorial.
{% endhint %}

{% page-ref page="resourcepack-on-dropbox.md" %}

## What is the difference between self-host and external-host?

Difference is that with self-host you can download the pack directly from your server without having to upload it to a website each time you make a small change.

{% hint style="info" %}
`self-host` is really useful when you are configuring the resourcepack on your test server on your PC. Because you just have to use command `/iazip` and you'll see changes applied ingame almost instantly.
{% endhint %}

{% page-ref page="../tips-for-fastest-usage.md" %}

## How can I configure the self host?

* Check in your hosting service panel if you can get an additional port, if not please ask hosting service support to provide your one.
* After you obtained a port you can open `config.yml` and set like this:

```yaml
  self-host:
    enabled: true
    server-ip: '127.0.0.1'
    pack-port: 8163
  external-host:
    enabled: false
```

* you have to replace `127.0.0.1` with ... your server IP
* and replace `8163` with the additional port you obtained.
* So for example if my ip is `123.456.789.0` and my additional port is `8080` I will set it like this:

```yaml
  self-host:
    enabled: true
    server-ip: '123.456.789.0'
    pack-port: 8080
  external-host:
    enabled: false
```

{% hint style="warning" %}
**Additional port** is not the same as your server port \(the one your users use to connect\).
{% endhint %}

{% hint style="info" %}
If you are testing the plugin on your PC you can leave default config, because 127.0.0.1 means "this pc", so plugin will look for the resourcepack zip directly in your PC.
{% endhint %}

{% hint style="danger" %}
Do not forget to use `/iazip` **everytime** you edit a **texture**, a 3D **model**, a **sound**...  ****or you won't see any change obviously.
{% endhint %}

