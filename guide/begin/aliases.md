---
description: Aliases
---

# Aliases

## Default Aliases

```javascript
bot.command({
name: "name",
aliases: ['name2','name3'], // If you want to do only one aliase you can do ['name2'] or just 'name2'
code: `code`
})
```

## Aliases for Command Handler

{% hint style="danger" %}
Re-update your server.js to this:
{% endhint %}

```javascript
const Aoijs = require("aoi.js")
 
const bot = new Aoijs.Bot({
token: "TOKEN", 
prefix: "!" 
});
 
bot.onMessage();

bot.loadCommands(`./commands/`);
```

### Aliases in your file.js in commands folder

```javascript
module.exports = ({
name: "name",
aliases: ['name2','name3'],
code: `code`
})
```

