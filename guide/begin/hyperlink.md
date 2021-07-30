---
description: Setting a Hyperlink in an embed's description.
---

# Hyperlink

### How it works

```javascript
[A text field(https://validlink.com 'hover text field')
```

{% hint style="danger" %}
Hyperlinks only work inside $description and embed fields.
{% endhint %}

### Usage

{% tabs %}
{% tab title="index.js" %}
```javascript
bot.command({
name: "hyperlink", 
code: `
$description[[Package](https://www.npmjs.com/package/aoi.js 'click')]` 
})
```
{% endtab %}
{% endtabs %}

