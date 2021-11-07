---
description: only the specified user IDs will be able to execute the command
---

# $onlyForIDs

This function only runs the command if the author's id matches to the specified ids

```text
$onlyForIDs[id1;id2;..;error when blocked]
```

```javascript
bot.command({
name: "special",
code: `Special Command
$onlyForIDs[535566311942651924;:x: You can't run this command]`
})
```

