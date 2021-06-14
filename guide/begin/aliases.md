---
description: Aliases
---

# Aliases

## Default Aliases

```javascript
bot.command({
name: "name",
aliases: ['name2','name3'], // If you want to do only one alaise you can ['name2'] or just 'name2'
code: `code`
})
```

## Aliases for Command Handler

{% hint style="danger" %}
Re-update your server.js to this:
{% endhint %}

```javascript
const dbd = require("dbd.js")
 
const bot = new dbd.Bot({
token: "TOKEN", 
prefix: "!" 
})
 
bot.onMessage()
 
const fs = require('fs')

const folders = fs.readdirSync("./commands/")

for (const files of folders) {
const folder = fs.readdirSync(`./commands/${files}/`).filter(file => file.endsWith(".js"))

for (const commands of folder) {
const command = require(`./commands/${files}/${commands}`) 
bot.command({
name: command.name,
aliases: command.aliases, // Here we make the bot read aliases correctly.
code: command.code
})
}
}
```

### Aliases in your file.js

```javascript
module.exports = ({
name: "name",
aliases: ['name2','name3','etc'],
code: `code`
})
```

