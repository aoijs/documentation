---
description: Returns the Database Ping.
---

# $dbPing

This function returns the database ping in Milliseconds. 

Example response: 3 \(for 3 ms\)

```text
bot.command({
name: "database", 
code: `
Database Ping: $dbPing`
})
```

