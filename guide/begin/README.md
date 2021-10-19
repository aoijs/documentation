# Getting Started

## Installation
> **⚠ Node.JS 12.0.0 or newer is required.**

<table>
  <tr>
  <th align="left">Terminal</th>
  </tr>
  <tr>
  <td>

  ```bash
  npm install aoi.js
  ```

  </td>
  </tr>
</table>

Once this has installed you can begin the following file `index.js` to setup Aoi.JS.

<table>
  <tr>
  <th align="left">index.js</th>
  </tr>
  <tr>
  <td>

  ```javascript
  const aoijs = require("aoi.js")

  const bot = new aoijs.Bot({
    token: "TOKEN", //Discord Bot Token
    prefix: "PREFIX" //Discord Bot Prefix
  })

  bot.onMessage() //Allows to execute Commands

  bot.command({
    name: "ping", //Trigger name (command name)
    code: `Pong! \`$ping\`ms` //Code
  })

  bot.readyCommand({
    channel: "", //You can use this or not
    code: `$log[Ready on $userTag[$clientID]]` //Example Ready on Client
  })
  ```

  </td>
  </tr>
</table>

> You must enter a prefix via `PREFIX`
>
> You must enter a valid Discord Bot Token via `TOKEN`

> ✅ Just simple as that you can begin using Aoi.JS

## package.json

> ⚠ In most Hosting Services you will need a `package.json` file

If you need a example, there's a quick example to use.

<table>
  <tr>
  <th align="left">package.json</th>
  </tr>
  <tr>
  <td>

  ```json
  {
    "name": "-asdf",
    "version": "1.0.0",
    "description": "",
    "main": "index.js",
    "scripts": {
      "start": "node index.js"
    },
    "engines": {
      "node": "12.x"
    },
    "author": "",
    "license": "ISC",
    "dependencies": {
      "aoi.js": "^4.5.0"
    }
  }
  ```
  </td>
  </tr>
</table>

> ℹ️ `4.5.0` can be changed to any version number as you want.
