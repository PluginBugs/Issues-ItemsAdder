# 👌🏻权限

* 玩家

  * /ia
    * `ia.user.ia`
  * /iarecipe
    * `ia.user.iarecipe`
  * /iatexture
    * `ia.user.iatexture`
  * 合成
    * `ia.user.craft.PERMISSION` \(如果不想区分，可以给 ia.user.craft.\*\)
    * 想了解更多关于物品权限[ 请点击这里](adding-content/advanced/item-properties/basic/item-permission.md)
  * 设置 /ia 菜单中内容是否可见
    * `ia.user.ia.PERMISSION` \(如果不想区分，可以给 ia.user.ia.\*\)
    * 想了解更多关于物品权限[ 请点击这里](adding-content/advanced/item-properties/basic/item-permission.md)
    * `ia.user.iasearchgui` 允许玩家使用 /ia 菜单中的搜索功能
    * 你也可以为每一个类别设置权限，参见[ /ia GUI](ia.md)
  * 表情 \(font images\)
    * **/iaimage /emoji, /iaemoji, /e** 打开表情菜单 （通过书的形式展示所有的表情和字体）
      * `ia.user.image.gui`
    * **/iaimage** **/emoji &lt;text&gt;, /iaemoji &lt;text&gt;, /e &lt;text&gt;** （允许使用tab补全）
      * `ia.user.image.hints`
    * 允许聊天中使用表情
      * `ia.user.image.chat`
    * 允许指令中使用表情
      * `ia.user.image.command`
    * 允许告示牌中使用表情
      * `ia.user.image.sign`
    * 允许书本中使用表情
      * `ia.user.image.book`
    * 允许铁砧中使用表情
      * `ia.user.image.anvil`
    * 允许聊使用表情
      * `ia.user.image.use.<font image name>`
      * 例如： `ia.user.image.use.heart`

  ​

* 管理
  * /iaget
    * `ia.admin.iaget`
  * /iagive
    * `ia.admin.iagive`
  * /iadrop
    * `ia.admin.iadrop`
  * /iaremove
    * `ia.admin.iaremove`
  * /iatag
    * `ia.admin.iatag`
  * /iareload
    * `ia.admin.iareload`
  * /iablock （获取你正在看的方块的信息）
    * `ia.admin.iablock`
  * /iadurability
    * ia.admin.iadurability
  * 编辑权限 （/ia 中的编辑按钮）
    * `ia.admin.edit`
  * /iaplayerstat write （设置玩家的特定信息）
    * `ia.admin.iaplayerstat.write`
  * /iaplayersta read （读一个玩家的特定信息）
    * `ia.admin.iaplayerstat.read`
  * /iainfo （获取插件相关信息）
    * `ia.admin.iainfo`
  * /iakill &lt;mob\|all&gt; （杀死所有自定义怪物）
    * `ia.admin.iakill`
  * /iasummon &lt;mob&gt; \[amount\]
    * `ia.admin.iasummon`
  * /iaspawntree &lt;tree&gt;
    * `ia.admin.iaspawntree`
  * /iaplaytotemanimation &lt;totem&gt; &lt;player&gt;
    * `ia.admin.iatotemanimation`
* 其他
  * 无视拒绝资源包被踢出
    * `ia.resourcepack.bypasskick`
  * 无视玩家放置的方块不掉落物品
    * `ia.admin.bypassblockplaceloot`

