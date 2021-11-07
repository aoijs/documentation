---
description: Set a global variable value for everyone to access
---

# $setVar

This function set's a global variable

```javascript
$setVar[variable;value]
```

```javascript
bot.command({
name: "setVar",
code: `Set a global var
$setVar[globalXP;25]` //This value will be the same for all users in all servers
})
```

{% hint style="danger" %}
THIS IS NOT A GLOBAL USER VARIABLE
{% endhint %}

