---
description: Parse given in ms to date or time
---

# $parseDate

This function returns the date/time for the given ms

```text
$parseDate[ms;date/time]
```

```javascript
bot.command({
name: "parseDate",
code: `$parseDate[29835039430;time]`
/*
Date/Time Examples:
time - 55 years 5 months 6 days 1 hour 32 minutes and 56 seconds
date - Wed Dec 30 2020 01:34:42 GMT+0000 (Greenwich Mean Time)
*/
})
```



