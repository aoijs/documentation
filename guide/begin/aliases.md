---
description: Setting up Aliases for your Commands.
---

# Aliases

### Default Aliases

{% tabs %}
{% tab title="index.js" %}
```javascript
bot.command({
name: "name",
aliases: ['name2','name3'], // If you want to do only one aliase you can do ['name2'] or just 'name2'
code: `code`
})
```
{% endtab %}
{% endtabs %}

### Aliases for Command Handler

{% hint style="danger" %}
Re-update your index.js to this:
{% endhint %}

{% tabs %}
{% tab title="index.js" %}
```javascript
const aoijs = require("aoi.js")

const bot = new aoijs.Bot({
token: "TOKEN", 
prefix: "PREFIX" 
});

bot.onMessage();

bot.loadCommands(`./commands/`); //YOU MUST HAVE.
```
{% endtab %}
{% endtabs %}

{% hint style="info" %}
Above is an example of how it should look in your main index.
{% endhint %}

### Aliases in your `command.js` in commands folder

{% tabs %}
{% tab title="command.js" %}
```javascript
module.exports = ({
name: "name",
aliases: ['name2','name3'], //This can be anything you want.
code: `code`
})
```
{% endtab %}
{% endtabs %}

