---
description: Sets a server cooldown
---

# $serverCooldown

This function creates a cooldown for the command in the current guild

```text
$serverCooldown[time;error when cooldown activated]
```

{% hint style="info" %}
%time% returns the remaining cooldown time
{% endhint %}

```javascript
bot.command({
name: "serverCooldown",
code: `Cooldown command
$serverCooldown[15s;Theres a cooldown!]`
})
```

