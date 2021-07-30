---
description: Checks if the given user ID DM's are enabled. (Returns true or false)
---

# $isUserDMEnabled

#### Usage

```text
$isUserDMEnabled[userID (optional)]
```

#### Example

```javascript
bot.command({
    name: "is-dm-enabled"
    code: `$isUserDMEnabled[$authorID]` //Returns true or false depending on author.
})
```

