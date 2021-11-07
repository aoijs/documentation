---
description: Set's the bots status
---

# $setStatus

This function sets the bot's status

```text
$setStatus[text;type;status]
```

{% hint style="warning" %}
Types: "PLAYING", "LISTENING", "WATCHING", "STREAMING", "COMPETING"
{% endhint %}

{% hint style="warning" %}
STATUS: "dnd", "idle", "online", "invisible"
{% endhint %}

```javascript
bot.command({
name: "setStatus",
code: `$setStatus[music;LISTENING;dnd] Successfully changed the bot's status <3`
})
```

