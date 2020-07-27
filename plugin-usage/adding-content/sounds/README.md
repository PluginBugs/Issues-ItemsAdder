# Sounds

### Step 1

{% page-ref page="convert-sound-to-.ogg.md" %}

* open plugins\ItemsAdder\data\resource\_pack\assets folder
* open your [namespace](../creating-your-namespace.md) folder
* create a new folder called sounds
* put your .ogg file in there \(you can also create another folder to organize your sounds, for example "effects" folder, "music" folder...\)

for example I have a file named cdk\_sunday.ogg and I put it into a new music\_disc folder.  
So now I have `plugin\ItemsAdder\data\resource_pack\assets\NAMESPACE\sounds\music_disc\cdk_sunday.ogg`

### Step 2

* open plugins\ItemsAdder\data\resource\_pack\assets folder
* open your [namespace](../creating-your-namespace.md) folder
* create a new file named `sounds.json` \(or open it if you already created\)
* this file is a json file, you MUST write it corretly or it won't work. If you need info about Json files please search online.

To add your sound into the file you just have to do this:

```javascript
{
	"music_disc.cdk_sunday":{
		"sounds":[
			"itemsadder:music_disc/cdk_sunday"
		]
	}
}
```

Now I explain each part of the code I wrote.  
This is the sound name, you will use it in every part of the plugin and also in Minecraft vanilla [/playsound ](https://www.digminecraft.com/game_commands/playsound_command.php)command

```javascript
"music_disc.cdk_sunday":{
```

This is the list of sound files Minecraft will play when you call the sound name.  
Minecraft will play one of these sounds randomly \(only if you set more than one sound\).

```javascript
"sounds":[
			"itemsadder:music_disc/cdk_sunday"
		]
```

For example if you want to have random sounds for the same sound name you just have to create multiple .ogg files and put them like this:

```javascript
"sounds":[
			"itemsadder:music_disc/cdk_sunday_1",
			"itemsadder:music_disc/cdk_sunday_2",
			"itemsadder:music_disc/test_file"
		]
```

## How can I add multiple sounds in the sounds.json file?

It's easy, the next time you want to add a sound you just have to add a comma at the end, like this.  
\(I'm referring to line 6 comma\)

```javascript
{
    "music_disc.cdk_sunday":{
        "sounds":[
            "itemsadder:music_disc/cdk_sunday"
        ]
    },
    "music_disc.vidian_aether_theories":{
        "sounds":[
            "itemsadder:music_disc/vidian_aether_theories"
        ]
    }
}
```

{% hint style="warning" %}
If you want to be sure not to make mistakes use this website to check if your Json file is good or has errors: [https://jsonformatter.curiousconcept.com/](https://jsonformatter.curiousconcept.com/)
{% endhint %}

