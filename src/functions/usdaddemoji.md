---
description: Add a Emoji to the Guild.
---

# $addEmoji

This function takes care of automatically adding an emoji to the server using the provided URL.

{% hint style="warning" %}
The URL of the original image must be under 256kb in size.
{% endhint %}

#### Fields:

This function has 3 properties who are required and another 2 optional.  
The order it's the next:

1. guildId \(Required\) 
2. URL \(Required\)
3. Name \(Required\)
4. reason \(Optional\)
5. roleIDs \(optional\)

Raw Usage: `$addEmoji[guildId;url;name;reason;roleId1;roleId2;...]`

#### Options:

* `guildId` - The guild ID for the emoji will be added
* `URL` - The url of the image/gif that's being converted to an emoji
* `Name` =&gt; The name of the emoji
* `reason` =&gt; The reason why emoji added
* `roleIDs` =&gt; Array of roles' IDs they should have access to that emoji. Only members with these role would have access to see and use that emoji. Leave it empty to set to everyone.

An example of the use should be the next:

#### Usage

```javascript
bot.command({
    name: "add-emoji",
    code: `$addEmoji[$guildID;https://cdn.discordapp.com/emojis/786763619438166036.png;shy_bear;Because why not;849217373214474253]`
});
```

{% hint style="warning" %}
URL NEEDS to end in `.gif`, `.png` or `.jpg`
{% endhint %}

