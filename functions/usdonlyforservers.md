---
description: The command will only execute in the specified guild ids
---

# $onlyForServers

This function will only execute if the current guild id matches with the specified guild ID

```text
$onlyForServers[id1;id2;...;error when blocked]
```

```javascript
bot.command({
name: "special",
code: `Special Command
$onlyForServers[773352845738115102;:x: You can't run this command]`
})
```

