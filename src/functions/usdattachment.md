---
description: Adds an attachment to the message.
---

# $attachment

This function allows you to add 'attachments' to a message, like images or videos.

#### Fields

This function has 1 field

1. URL \(Required\)

Raw Usage: `$attachment[url]`

#### Options

* URL - The url of the image/gif/video of which you want the bot to send

#### Usage

```javascript
bot.command({
    name: "dog",
    code: `$attachment[https://cdn.discordapp.com/attachments/773357374328012840/780585674541105152/20201116_133035.jpg] Take a pic of Kuba's dog!`
});
```

