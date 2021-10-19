# $nodeVersion

This function returns the current Node.js verion the server is using.

#### Example Command:

The function would return v12.22.1 as example.

```js
bot.command({
name: "node",
code: `
current version: $nodeVersion
`
})
```

