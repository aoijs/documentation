---
description: Gets information on an embed
---

# $getEmbed

This function gets the &lt;property&gt; of the embed

#### Fields

This function has 3 required fields.

1. Channel ID \(Required\)
2. Message ID \(Required\)
3. Property \(Required\)

Raw usage: `$getEmbed[Channel ID;Message ID;Property]`

#### Options

* Channel ID - Channel Where the message is located.
* Message ID - Message which you want to get the embed info.
* Property \(type, title, description, url, color, timestamp, fields, fvalue, thumbnail, image, video, author, provider, footer, files, createdAt, hexColor, length\) - The embed property you want to get.

#### Usage

```javascript
bot.command({
name: "getEmbed",
code: `Embed Title Info: $getEmbed[773357387062968400;780877316380688444;title]`
})
```

