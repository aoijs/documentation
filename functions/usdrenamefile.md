---
description: This function simply renames the file that you provided.
---

# $renameFile

Here is the usage:

```text
$renameFile[(old File Name);(New File Name)]
```

Now lets rename a file.

```javascript
bot.command({
name: "rename",
code: `
$renameFile[config.json;config.txt]
//This will rename config.json to config.txt if it exists.
`
})
```

Now lets rename a file in a directory.

```javascript
bot.command({
name: "rename",
code: `
$renameFile[config/data/data.json;config/data/data.txt]
//Renames the file to data.txt
`
})
```

You can also move the renamed file to somewhere else.

```javascript
bot.command({
name: "rename",
code: `
$renameFile[config/data/data.json;config/beta/data.txt]
//This will move the data.txt file to config/beta directory.
`
})
```

