# Custom Events

aoi.js has `CustomEvent` class to add custom events to aoi.js that will execute a command for that event , whenever the event is emitted.

This adds 2 new functions:

 [**`$eventData`**](../functions/usdeventdata.md) and [**`$eventEmit`**](../functions/usdeventemit.md)

## Usage

```ts
const event : CustomEvent = new CustomEvent(
    bot:Bot,
)
```

### bot 

<table>
  <tr>
    <th>Type</th>
    <td>Bot</td>
  </tr>
  <tr>
    <th>Description</th>
    <td>aoi.js' Bot Class</td>
  </tr>
    <tr>
    <th>Required</th>
    <td>yes</td>
  </tr>
  <tr>
    <th>Default</th>
    <td>N/A</td>
  </tr>
</table>

## Basic Setup

```js
const  { CustomEvent , Bot } = require("aoi.js");

const bot = new Bot({
    token : "DISCORD BOT TOKEN",
    prefix: "DISCORD BOT PREFIX",
    intents: [ "guilds", "guildMessages" ],
});

bot.onMessage();

const event = new CustomEvent(bot);

event.listen("pain");

event.command({
    name: "this is pain",
    listen: "pain",
    code:`
        $log[ Pain Event Was Executed By $eventData[[0]] ]
    `
});

bot.command({
    name: "emit-pain",
    code:`
        $eventEmit[pain;$username]
    `
})
```

