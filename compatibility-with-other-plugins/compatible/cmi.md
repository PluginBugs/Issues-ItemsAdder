# CMI

{% hint style="info" %}
## If you're using CMI chat feature you have to read this.
{% endhint %}

## Emoji

Open config.yml of **ItemsAdder** and set this:

```yaml
font_images:
  chat:
    enabled: true
    replace-only-packets: true
```

## Ranks

1. Open config.yml of **CMI** and set this \(I set `%vault_prefix%` placeholder instead of **CMI** `{prefix}`\)

```yaml
GeneralFormat: '%vault_prefix% &f{displayName}&7: &r{message}'
```

2. Download [PlaceholderAPI](https://www.spigotmc.org/resources/placeholderapi.6245/) and [Vault](https://github.com/MilkBowl/Vault/releases/latest)  
3. Install them and Restart  
4. execute this command  `/papi ecloud download Vault`  
5. execute this command `/papi reload`

Done

