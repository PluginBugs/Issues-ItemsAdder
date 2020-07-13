# Le resourcepack ne se charge pas

#### Resourcepack not loading, I get an error in chat <a id="resourcepack-not-loading-i-get-an-error-in-chat"></a>

* Check if you have another plugin that uses **custom resourcepacks**, if you have please **disable** its **resourcepack** feature or ItemsAdder won't be able to apply the pack correctly \(you can make them compatible if you've a minimum knowledge on how to merge resourcepacks manually, be sure to not replace ItemsAdder files and you're done. The pack folder of ItemsAdder is `resouce_pack`\)
* Minecraft limits servers resourcepacks size to 50MB, be sure to compress your textures and your music files before creating the zip file.
* Be sure that your`custom_url`is a **direct** download link to the zip file. If you paste the link on your browser \(Firefox/Chrome\) you must instantly see the download start, if you see a download page with buttons it's wrong. Please upload it on Dropbox, generate the download/share link and change `dl=0` to `raw=1` at the end of link.
* Be sure to follow all [tutorial ](../plugin-usage/resourcepack-hosting/)steps
* Be sure the port is opened if you use self-host.

