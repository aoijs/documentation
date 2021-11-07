---
description: >-
  Returns specified user ID's username, if no argument given, returns author's
  username
---

# $username

This function returns the authors/give user id's username

```text
$username[user ID (optional)]
```

```javascript
bot.command({
name: "username",
code: `608358453580136499 username is $username[608358453580136499]!`
//Returns Leref
})
```

