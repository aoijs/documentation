---
description: Returns the user's discord status
---

# $status

```javascript
$status[userID (optional)]
```

{% hint style="danger" %}
Must enable discord presence intents
{% endhint %}

```javascript
bot.command({
name: "status",
code: `Your Status: $status`
})
```

{% hint style="warning" %}
Bot Returns Either: dnd, online, invisible, idle
{% endhint %}

