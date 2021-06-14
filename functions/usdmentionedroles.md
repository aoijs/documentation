---
description: 'Returns the ID of mentioned roles, such as $mentioned function.'
---

# $mentionedRoles

This function returns the id of the mentioned role

```javascript
$mentionedRoles[arg]
```

```javascript
bot.command({
name: "role",
code: `$mentionedRoles[1]`
/*
    Arg Numbers
1- Return the first mentioned
2- Return the second mentioned
and so on
*/
})
```

