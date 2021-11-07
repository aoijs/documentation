---
description: Displays true or false depending if the channel is a ticket or not.
---

# $isTicket

This function will return true or false depending if the channel is a tiket or not.

Raw usage: `$isTicket` or `$isTicket[Channel ID]`

Example:

```javascript
bot.command({
    name: "istiket",
    code: `
Is this channel a tiket?
> $isTicket
    `
})
```

