---
description: Gets the user's custom status state. (if any)
---

# $getCustomStatus

This function returns the custom status of the given user, if they have one

```text
$getCustomStatus[userID (optional);state/emoji]
```

{% hint style="info" %}
state - The message, emoji - the emoji
{% endhint %}

```javascript
bot.command({
name:"customstatus",
code:`$getCustomStatus[502968724207304714;state]`
})
```

