# Aliases

### Default Aliases

<table>
  <tr><th align="left">
    index.js
  </th></tr>
  <tr><td>

  ```javascript
  bot.command({
    name: "name",
    aliases: ['name2','name3'], // If you want to do only one aliase you can do ['name2'] or just 'name2'
    code: `code`
  })
  ```
  </td></tr>
</table>

### Aliases for Command Handler

> ❗ Re-update your index.js to this:

<table>
  <tr><th align="left">
    index.js
  </th></tr>
  <tr><td>

  ```javascript
  const aoijs = require("aoi.js")

  const bot = new aoijs.Bot({
    token: "TOKEN", 
    prefix: "PREFIX"
  });

  bot.onMessage();

  bot.loadCommands(`./commands/`); //YOU MUST HAVE.
  ```
  </td></tr>
</table>

> ℹ️ Above is an example of how it should look in your main index.

### Aliases in your `command.js` in commands folder

<table>
  <tr><th align="left">
    command.js
  </th></tr>
  <tr><td>
    

  ```javascript
  module.exports = ({
    name: "name",
    aliases: ['name2','name3'], //This can be anything you want.
    code: `code`
  })
  ```
  </td></tr>
</table>
