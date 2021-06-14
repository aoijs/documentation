---
description: Closes a ticket
---

# $closeTicket

This function closes a ticket/channel made by [$newTicket](usdnewticket.md)

#### Fields

This function has 1 field

1. Error Message \(Required

Raw Usage: `$closeTicket[error message]`

#### Options

* Error Message - This will appear when the function has been ran in a non-ticket channel

#### Usage

```javascript
bot.command({
name: "close",
code: `$closeTicket[This is not a ticket!]`
})
```

