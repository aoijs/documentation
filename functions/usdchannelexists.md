---
description: Returns true or false if it finds the channel
---

# $channelExists

This function will check if the delivered ID is from an existing channel or not, delivering true or false.

#### Fields

This function has 1 field

1. channelID \(Required\)

Raw Usage: `$channelExists[channelID]`

#### Options

* channelID - The channel we're checking if it exists

{% hint style="warning" %}
This function is global, this means it will search for channels not only in this guild, it will search for the channel in all the guilds your bot is on.
{% endhint %}

#### Usage

```javascript
bot.command({
    name: "channel",
    code: `$channelExists[$message]`
});

/*
    This will search for the channel with the ID the user
    provided in the message.
*/
```

