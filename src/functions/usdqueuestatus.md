---
description: Returns the current Queue Status.
---

# $queueStatus

This function will tell you the current status of the queue, if it's playing, paused or idle.

Example:

```javascript
bot.command({
    name: "queuestatus",
    code: `
    The queue is currently $queueStatus
    `
})
```

