---
description: Creates a ticket channel.
---

# $newTicket

This function creates a new ticket channel for the author.

```text
$newTicket[ticket name;ticket message (optional);category id (optional); return ticket id (yes/no);error message (optional)]
```

```javascript
bot.command({
name: "ticket",
code: `Ticket Created!
$newTicket[ticket-$random[100;10000];Hello, Please mention a staff member!;773356383625150505;no;Error!]
`
})
```

