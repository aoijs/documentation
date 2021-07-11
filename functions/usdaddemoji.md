---
description: Adds a emoji to the guild.
---

# $addEmoji

### Usage
```
$addEmoji[URL;name;(optional) returnEmoji (yes/no);(optional) roleIDs]
```

#### Options:

* `URL` - The URL of the image/gif that's being converted to an emoji.
* `name` - The name of the new emoji.
* `returnEmoji (yes/no)` - Whether to return the the emoji that was newly created.
* `roleIDs` - List of roleIDs that should have access to this emoji. Only members with the roles will have access to see and use that emoji. Leave it empty to set to everyone. Separate IDs using `;`.

### Example

```javascript
bot.command({
    name: "add-emoji",
    code: `$addEmoji[https://cdn.discordapp.com/emojis/786763619438166036.png;shy_bear;yes]`
});
```

#### Example result:

![](../.gitbook/assets/mtt45fdb8q.png)

{% hint style="warning" %}
The URL needs to end with `.gif`, `.png` or `.jpg`.
{% endhint %}

{% hint style="warning" %}
The URL of the original image must be under 256kb in size.
{% endhint %}
