---
description: Checks if given user ID is banned. (Returns true or false)
---

# $isBanned

This  function checks if the given user is banned or not. Returns boolean

#### Usage

```text
$isBanned[user ID;guild ID (optional)]
```

#### Example

```javascript
bot.command({
name: "isBanned",
code: `Is banned: $isBanned[608358453580136499]`
})
```

