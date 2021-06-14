---
description: Returns when the User Joined the Guild.
---

# $memberJoinedDate

This function returns when the user joined the current guild

```text
$memberJoinedDate[userID;time/date/ms]
```

```javascript
bot.command({
name: "joinndate",
code: `$memberJoinedDate[$authorID;time]`
/*
time - 2 years 1 month 3 weeks 3 days 6 hours 42 minutes and 6 seconds
date - Thu Jan 17 2019 21:09:19 GMT+0000 (Greenwich Mean Time)
*/
})
```



