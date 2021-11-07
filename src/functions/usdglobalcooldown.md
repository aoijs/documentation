---
description: 'Set a Global cooldown, with all Guilds'
---

# $globalCooldown

$globalCooldown\[time;error when cooldown activated\]

{% hint style="info" %}
%time% returns the remaining cooldown time
{% endhint %}

```text
bot.command({
name: "hello", 
code: `
$description[Hello!]
$globalCooldown[1m;Hey, you need to wait 1m!]
})
```

