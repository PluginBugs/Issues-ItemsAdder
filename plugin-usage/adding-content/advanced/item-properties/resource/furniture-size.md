# Furniture size

## How can I adjust the furniture position when placed?

If you want to adjust it you just have to use [Blockbench](creating-3d-models.md) as usual and:

![](../../../../../.gitbook/assets/immagine%20%289%29.png)

1. click on **display** on the right
2. click on the **armorstand icon** on the left
3. click on the **smile face** \(**head**\) on the left
4. **move** your model on the armorstand **bottom** \(it's the **ground**\)

### Too small furniture

If your furniture is **too small** bug you want it **bigger** and with bigger **hitbox** just set this to **false**.  
If you instead want a **small furniture** with small hitbox just set it to true

{% tabs %}
{% tab title="Big furniture" %}
```yaml
behaviours:
  furniture:
    small_hitbox: false
```
{% endtab %}

{% tab title="Small furniture" %}
```
behaviours:
  furniture:
    small_hitbox: true
```
{% endtab %}
{% endtabs %}

#### and set this is [BlockBench](creating-3d-models.md)

{% tabs %}
{% tab title="Big furniture" %}


![](../../../../../.gitbook/assets/immagine%20%288%29.png)
{% endtab %}

{% tab title="Small furniture" %}


![](../../../../../.gitbook/assets/immagine%20%2810%29.png)
{% endtab %}
{% endtabs %}

