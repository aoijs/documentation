---
description: Returns all the server IDs the bot is in
---

# $serverIDs

```text
$serverIDs[separator (optional)]
```

{% hint style="info" %}
Separator is the symbol that separates each server ID
{% endhint %}

```javascript
bot.command({
name: "serverIDs",
code: `Server IDs: $serverIDs[,]`
//will return: serverid,serverid,serverid,etc
})
```

