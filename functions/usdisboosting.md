---
description: Check if the given user ID is boosting. (Returns true or false)
---

# $isBoosting

#### Usage

```text
$isBoosting[User ID]
```

#### Example

```javascript
bot.command({
name: "isboost", 
code: `$isBoosting[$authorID]` //Returns true or false depending on author
})
```

