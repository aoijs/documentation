---
description: Deletes bots message in the specified time
---

# $deleteIn

This function deletes the bot's message in the specified time

#### Fields

This function has 1 field

1. Time \(Required\)

Raw Usage: `$deleteIn[time]` 

Options

* Time - The amount of time left until it deletes the bot message

#### Usage

```javascript
bot.command({
name: "deleteIn",
code: `Message wil be deleted in 5 seconds
$deleteIn[5s]`
})
```

#### Time Suffixes

* s - Seconds
* m - Minutes
* h - Hours
* d - Days
* w - Weeks

