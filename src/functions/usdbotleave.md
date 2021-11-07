---
description: Forces the bot to leave the specified server.
---

# $botLeave

This function makes the bot leave the current / specified server

#### Fields

This function has 1 optional field

1. Server ID \(Optional\)

Raw Usage: `$botLeave[serverID (optional)]`

#### Options

* Server ID - The server of which the bot is going to leave from

{% hint style="danger" %}
Using this function will make your bot leave the specified server, we recommend using $onlyForIDs\[Your ID;Only for my owner\]
{% endhint %}

#### Usage

```javascript
bot.command({
    name: "exit",
    code: `
    $botLeave
    $onlyForIDs[278342221202194434;You're not Chiwi!]
    `
});

// I just used my ID but you can replace it with yours.
```



