---
description: Unbans a user from the server
---

# $unban

This function unbans the user from the guild

```text
$unban[guildID;user ID;reason (optional)]
```

{% hint style="info" %}
Reason will show up in audit logs
{% endhint %}

```javascript
bot.command({
name: "unban",
code: `Unbanned the user with the ID of 535566311942651924
$unban[$guildID;535566311942651924]`
})
```

