---
description: Sets a slowmode to the given channel
---

# $slowmode

This function sets a cooldown to the given channel ID. `0` will set the cooldown to none

```text
$slowmode[time/0;channelID]
```

{% hint style="danger" %}
Discord does not allow you to go over 6 hours
{% endhint %}

```javascript
bot.command({
name: "slowmode",
code: `Set the channel slowmode
$slowmode[5m;$channelID]` //Sets the current channel slowmode to 5 minutes
})
```

