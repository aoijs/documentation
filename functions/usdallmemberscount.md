---
description: Returns the total count of users in all guilds your bot's in.
---

# $allMembersCount

This function is responsible for showing the number of users that your bot has registered throughout all the communities in which it is currently.

#### Usage

```javascript
bot.command({
    name: "usercount",
    code: `This bot has $allMembersCount users!`
});
```

