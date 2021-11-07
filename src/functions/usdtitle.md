---
description: Adds a title to the embed
---

# $title

This function adds a title to the embed. URL for hyperlink

```text
$title[text;url (optional)]
```

{% hint style="danger" %}
Only use 1 per command.
{% endhint %}

```javascript
bot.command({
name: "title",
code: `$title[DBD.js]`
})
```

