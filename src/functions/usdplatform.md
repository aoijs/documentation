---
description: Returns the platform of the user using ID
---

# $platform

This function returns the platform the user is using discord with

```text
$platform[User ID]
```

```javascript
bot.command({
name: "platform",
code: `your platform is $platform[$authorID]`
})
```



