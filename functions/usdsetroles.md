---
description: Set some roles into guild member
---

# $setRoles

Sets some roles into a user using the User ID

Raw usage: `$setRoles[User ID;Role ID;Role ID;...]`

Example:

```javascript
bot.command({
    name: "set-roles",
    code: `
    The roles Support and Moderator have been set for Chïwi
    $setRoles[278342221202194434;773353339496169513;773353338854572073]
    `
```

