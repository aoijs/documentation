---
description: Executable only by the specified role IDs
---

# $onlyForRoles

This function makes the command only execute if the user has any of the roles specified

```text
$onlyForRoles[id1;id2;...;error when blocked]
```

```javascript
bot.command({
name: "special",
code: `Special command
$onlyForRoles[773353338393329675;:x: You can't run this command]`})
```

