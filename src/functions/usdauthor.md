---
description: Sets the author in an embed message and authorIcon if it's specified.
---

# $author

This function allows you to add an 'author' to the embed message and an icon or a URL if specified to the author.

#### Fields

Responding to your question, `$author` has 4 properties.

1. index.
2. text.
3. icon URL.
4. hyper link \(Optional field\)

Raw Usage: 
> `$author[index;text;icon url;hyperlink url (optional)]
`

#### Options

* Index - Multiple embeds support.
* Text - The author text.
* Icon URL - The url of the image next to the text.
* HyperLink URL - The URL of the redirect link.

{% hint style="warning" %}
The image URL needs to end with `.gif`, `.png`, `.jpeg` or `.jpg`
{% endhint %}

#### Usage
- Without Hyperlink:-

 ```javascript
bot.command({
    name: "embed",
    code: `$author[1;Aoi.js;$serverIcon]`
});
```

- With Hyperlink:-

```javascript
bot.command({
    name: "embed",
    code: `$author[1;Aoi.js;$serverIcon;https://aoi.js.org]`
});
```

