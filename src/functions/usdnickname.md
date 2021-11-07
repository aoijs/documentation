---
description: 'Returns the nickname, using a userID.'
---

# $nickname

This function returns the user's server nickname

```text
$nickname[User]
```

```javascript
bot.command({
name: "nickname",
code: `Your nickname is: $nickname[$authorID]`
})
```



