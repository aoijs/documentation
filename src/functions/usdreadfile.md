---
description: Returns the contents of the provided file
---

# $readFile

This function simply returns the contents of the provided file.

Here is the usage:

```text
$readFile[(file location)]
//This will send the contents of provided file in the channel.
```

Now lets get contents of a file.

```javascript
bot.command({
name: "read",
code: `
$readFile[config.json]
//This will send config.json contents in the channel.
`
})
```

Now lets get the contents of a file in directory.

```javascript
bot.command({
name: "read",
code: `
$readFile[config/text/data.json]
//This will send data.json contents in the channel.
`
})
```

