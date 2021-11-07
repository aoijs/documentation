---
description: Displays true or false depending if the server exists or not.
---

# $serverExists

This function will tell you if the server provided exists or not. Returns true or false.

Raw usage: `$serverExists[Guild ID]`

Example:

```javascript
bot.command({
    name: "server",
    code: `$serverExists[$message]`
})
/**
* This will check if the server ID
* (Provided in the message by the user)
* Is a valid guild ID or not.
*/
```

