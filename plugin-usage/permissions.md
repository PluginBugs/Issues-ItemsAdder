# 👌🏻Permissions

* Users

  * /ia
    * `ia.user.ia`
  * /iarecipe
    * `ia.user.iarecipe`
  * /iatexture
    * `ia.user.iatexture`
  * crafting
    * `ia.user.craft.PERMISSION` \(or to give all crafting permissions just use ia.user.craft.\*\)
    * for more info about item permissions please[ read this](adding-content/item-properties/basic/item-permission.md)
  * see item in /ia menu
    * `ia.user.ia.PERMISSION` \(or to give all /ia permissions just use ia.user.ia.\*\)
    * for more info about item permissions please[ read this](adding-content/item-properties/basic/item-permission.md)
    * `ia.user.iasearchgui` for the search GUI in /ia menu
    * You can also set a permission per category, please check [/ia GUI ](ia.md)page
  * emoji \(font images\)
    * **/iaimage /emoji, /iaemoji, /e** book GUI \(shows a book with the list of emojis/font images\)
      * `ia.user.image.gui`
    * **/iaimage** **/emoji &lt;text&gt;, /iaemoji &lt;text&gt;, /e &lt;text&gt;** \(shows a tab list with emojis based on searched term\)
      * `ia.user.image.hints`
    * Use emojis in chat
      * `ia.user.image.chat`
    * Use emojis in commands
      * `ia.user.image.command`
    * Use emojis in signs
      * `ia.user.image.sign`
    * Use emojis in books
      * `ia.user.image.book`
    * Use emojis in anvil rename field
      * `ia.user.image.anvil`
    * Permission to use an emoji
      * `ia.user.image.use.<font image name>`
      * Example: `ia.user.image.use.heart`

  ​

* Admin
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
  * /iablock \(get info about block you're looking at\)
    * `ia.admin.iablock`
  * /iadurability
    * ia.admin.iadurability
  * Edit permission \(edit button in /ia\)
    * `ia.admin.edit`
  * /iaplayerstat write \(writea player custom stat\)
    * `ia.admin.iaplayerstat.write`
  * /iaplayersta read \(read a player custom stat\)
    * `ia.admin.iaplayerstat.read`
  * /iainfo \(get info about the plugin\)
    * `ia.admin.iainfo`
  * /iakill &lt;mob\|all&gt; \(kill custom mobs\)
    * `ia.admin.iakill`
  * /iasummon &lt;mob&gt; \[amount\]
    * `ia.admin.iasummon`
* Other:
  * Bypass kick on refuse resourcepack
    * `ia.resourcepack.bypasskick`
  * Bypass player placed blocks can't drop loot
    * `ia.admin.bypassblockplaceloot`

