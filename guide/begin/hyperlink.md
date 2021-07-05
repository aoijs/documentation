---
description: Setting a Hyperlink in an embed's description.
---

# Hyperlink

{% hint style="warning" %}
Hyperlinks only work inside $description and embed fields.
{% endhint %}

```javascript
bot.command({
name: "hyperlink", 
code: `
$description[[Package](https://www.npmjs.com/package/aoi.js 'click')]` 
})
```

