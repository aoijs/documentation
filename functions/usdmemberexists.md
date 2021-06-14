---
description: Checks if given user ID is in the server.
---

# $memberExists

This function checks if the given user is in the current guild

```text
$memberExists[userID;Guild ID (Optional)]
```

```javascript
bot.command({
name: "ismember",
code: `$memberExists[535566311942651924]`
})
```



