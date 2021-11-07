---
description: Check if the user is boosting.
---

# $isBoosting

This function checks if the given user is boosting or not. Returns boolean

```text
$isBoosting[User ID]
```

```javascript
bot.command({
name: "isboost", 
code: `$isBoosting[$authorID]`
})
```

