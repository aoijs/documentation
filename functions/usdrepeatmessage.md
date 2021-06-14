---
description: Repeats the message for X amount of times
---

# $repeatMessage

This function repeats the &lt;message&gt; X amount of times

```javascript
$repeatMessage[times;message]
```

```javascript
bot.command({
name: "repeatMessage",
code: `$repeatMessage[5;Aoi.js is awesome]`
})
//Will resend 'Aoi.js is awesome' 5 times
```

