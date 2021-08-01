---
description: Setting up a Command Handler with Aoi.JS.
---

# Command Handler

### Adding Command Handler

{% tabs %}
{% tab title="index.js" %}
```javascript
bot.loadCommands(`./commands/`)
```
{% endtab %}
{% endtabs %}

{% hint style="info" %}
`commands` can be renamed to any directory folder.
{% endhint %}

{% tabs %}
{% tab title="index.js" %}
```javascript
$updatecommands //It will update the commands in the inital path.
```
{% endtab %}
{% endtabs %}

{% hint style="info" %}
`$updatecommands` can be used in `bot.loadCommands`
{% endhint %}

### Main File example

This is a example of how to use `bot.loadCommands(./commands/)` in your main index.

{% tabs %}
{% tab title="index.js" %}
```javascript
const aoijs = require("aoi.js")

const bot = new aoijs.Bot({
token: "TOKEN", //Discord Bot Token
prefix: "PREFIX" //Discord Bot Prefix
})
bot.onMessage() //Allows to execute Commands

bot.command({
name: "ping", //Trigger name (command name)
code: `Pong! $pingms` //Code
})

bot.readyCommand({
    channel: "", //You can use this or not
    code: `$log[Ready on $userTag[$clientID]]` //Example Ready on Client
})

bot.loadCommands(`./commands/`) //Allows Commands executed by `commands` folder
```
{% endtab %}
{% endtabs %}

### Command Handler Folder Setup

{% hint style="warning" %}
Create a folder named `commands`
{% endhint %}

![](../../.gitbook/assets/screenshot-2020-11-23-at-9.54.22-pm.png)

{% hint style="warning" %}
Make a subfolder
{% endhint %}

![Subfolder could be used as a category like a discord category](../../.gitbook/assets/screenshot-2020-11-23-at-9.57.28-pm.png)

{% hint style="warning" %}
Finally, make your file
{% endhint %}

![Name of file: commandName.js](../../.gitbook/assets/screenshot-2020-11-23-at-10.00.16-pm.png)

### Setting up a command with command handler.

{% tabs %}
{% tab title="example.js" %}
```javascript
module.exports = {
      name: "name",
      code: `your code/message`
}
```
{% endtab %}
{% endtabs %}

## Using different command types \(e.g. commands from callback events\) in the command handler

For other commands, like the bot.joinCommand, you just have to find the part behind `bot.`- take it and insert this part at the type option as in the example below. 

`bot.joinCommand` becomes `type: 'joinCommand',`   
`bot.userUpdateCommand` becomes `type: 'userUpdateCommand'` etc. 

The type line isn't needed for normal `bot.command` commands. Just write your code like in the code block above.

{% tabs %}
{% tab title="example.js" %}
```javascript
module.exports = {
      type: 'joinCommand',
      channel: "$systemChannelID",
      code: `your code/message`
}
```
{% endtab %}
{% endtabs %}

## Multiple commands in one file

If you want to use multiple commands inside one command handler file, do it like this:

{% tabs %}
{% tab title="example.js" %}
```javascript
module.exports = [{
  type: 'joinCommand',
  channel: '773364744240496640',
  code: `Welcome $userTag !!`
}, {
  name: 'ping',
  code: `Pong! $pingms`
}]
```
{% endtab %}
{% endtabs %}

