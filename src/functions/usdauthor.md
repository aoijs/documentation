---
description: Sets the author in an embed message and authorIcon if it's specified.
---

# $author

This function allows you to add an 'author' to the embed message and an icon to the author if a URL is specified.

#### Fields

Responding to your question, `$author[]` has 3 properties.

1. text.
2. icon URL.
3. Hyper link \(Optional\)

Raw Usage: `$author[text;icon url;url (optional)]`

#### Options

* Text - The author text
* icon URL - The url of the image next to the text
* HyperLink URL - The URL of the redirect link

{% hint style="warning" %}
The image URL needs to end with `.gif`, `.png` or `.jpg`
{% endhint %}

#### Usage

```javascript
bot.command({
    name: "embed",
    code: `$author[This is an example!;$authorAvatar]`
});

//with hyperlink

bot.command({
    name: "embed",
    code: `$author[Aoi.js;$serverIcon;https://aoi.js.org]`
});
```

