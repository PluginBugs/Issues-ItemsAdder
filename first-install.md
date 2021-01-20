# ⚙️首次使用

## 视频教程

{% embed url="https://youtu.be/GKGnlF4zZVg" %}

## 步骤 1

为防止对正在运行服务器产生一些不可预料的BUG，这里建议你在测试服务器上配置完后再移动到生产环境中。

{% hint style="danger" %}
如果你已经有了旧版本的 ItemsAdder （v1.0） 那么请先将目录 **plugins/ItemsAdder** 移动到 **ItemsAdder\_backup**
{% endhint %}

* 安装 [**ProtocolLib**](https://www.spigotmc.org/resources/protocollib.1997/)
* 安装 [**IALib**](https://www.spigotmc.org/resources/ialib.75974/)
* 安装 [**LightAPI**](https://www.spigotmc.org/resources/lightapi-fork.48247/)
* 将 **ItemsAdder.jar** 放到你的服务端插件目录中
* 开启服务器
* 让 ItemsAdder 首先完成**初始化** （国内用户尝试通过魔法上网来让ItemsAdder下载好默认的材质包和物品内容）
* 停止服务器

## 步骤 2

* 在插件加载完成后进入服务器并执行命令 `/iazip`
* 打开配置文件 plugins\ItemsAdder\config.yml
* 按照下面的链接来进行下一步的配置

{% page-ref page="plugin-usage/resourcepack-hosting/resourcepack-self-hosting.md" %}



{% hint style="warning" %}
当你想让插件更新资源包 `pack.zip`，请输入指令 `/iazip`
{% endhint %}

### 可选步骤

{% hint style="info" %}
如果想制作自定义的物品和方块等其他内容，可尝试访问以下内容。

{% page-ref page="faq/removing-default-stuff.md" %}
{% endhint %}



