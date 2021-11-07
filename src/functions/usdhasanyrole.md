---
description: checks if the user has at least one of the required roles
---

# $hasAnyRole

This function checks if the user has at least one of the specified roles, returns `true` or `false`.

Raw usage: `$hasAnyRole[Role ID;Role ID;...]` or `$hasAnyRole[User ID;Role ID;Role ID;...]`

Example:

```javascript
bot.command({
    name: "hasrole",
    code: `
    $hasAnyRole[773353338854572073;773353339496169513]
    `
}) // The role IDs are Support and Moderator in DBD.JS server
```

The command will return `true` if the author of the command has either `Support` or `Moderator` in Official DBD.JS Team Discord Server.

