# Resourcepack on DropBox

{% hint style="danger" %}
**Make sure you're not** using **UPPERCASE** or **special characters** in **items** names, **namespaces**, **texture files** \(**png**\) and **model files** \(**json**\)
{% endhint %}

{% hint style="danger" %}
**DO NOT USE** file **pack\_21521367.zip** or **precompressed\_example\_pack.zip** AS BASE!!!!  
YOU HAVE TO USE YOUR **pack.zip** FILE WHICH IS GENERATED AFTER **/iazip** COMMAND.  
You can find it here: `plugins/ItemsAdder/data/resource_pack/`
{% endhint %}

## How to upload your resourcepack to DropBox

One of the most famous is DropBox. It allows you to publish your files for free and it's really easy and fast.  
You just have to:

* Open [DropBox](https://dropbox.com/), register/login
* Open folder: `plugins/ItemsAdder/data/resource_pack/`
* Be sure you used command ****`/iazip` \(it's important because `/iazip`reloads the configs, updates the **pack.zip** file\)
* Drag and drop on **DropBox** the file **pack.zip**
* Press **Share**

![](../../.gitbook/assets/image%20%287%29.png)

* Press **Create link**

![](../../.gitbook/assets/image%20%282%29.png)

* Press **Copy link**
* For example if your link is [https://www.dropbox.com/blablabla?dl=0](https://www.dropbox.com/blablabla?dl=0) 
* Open `config.yml` of **ItemsAdder**
* Set it like this \(**I used the example URL, please use your own**\)

```yaml
resource-pack:
  apply-on-join: true
  kick-player-on-decline: false
  delay-ticks: 1
  self-host:
    enabled: false
    server-ip: '127.0.0.1'
    pack-port: 8163
  external-host:
    enabled: true
    url: 'https://www.dropbox.com/blablabla?raw=1'
```

* **THIS IS REALLY IMPORTANT**: **Use command** `/iareload` to reload configs \(in this case to reload the resourcepack download link\)
* **Use command** `/iatexture` on your game to refresh your texture ingame or use `/iatexture all` to refresh it for every player

{% hint style="danger" %}
Do not forget to use `/iazip` **everytime** you edit a **texture**, a 3D **model**, a **sound**... then **reupload** the pack on **Dropbox** and use **/iareload** or you won't see any change obviously.
{% endhint %}

{% hint style="warning" %}
**Change** the **file name each time** you **upload** a **new version** of the **resourcepack** to **force** the game to **redownload** the **new version**.  
If you **reupload** the **zip** file with the same and keep the **same URL** it **won't update** to each player.
{% endhint %}

