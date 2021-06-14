---
description: Returns Node.js version.
---

# $nodeVersion

This function returns the current Node.js verion the server is using.

#### Example Command:

The function would return v12.22.1 as example.

```text
bot.command({
name: "node",
code: `
current version: $nodeVersion
`
})
```

