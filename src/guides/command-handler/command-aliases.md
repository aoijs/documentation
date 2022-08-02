---
description: Setting up Aliases for your Commands.
---

# Aliases

### Usage:

```javascript
aliases: ['TEXT1','TEXT2']
```

{% tabs %}
{% tab title="index.js" %}
```javascript
bot.command({
name: "name",
aliases: ['name2','name3'],
code: `code`
})
```
{% endtab %}
{% endtabs %}

### Aliases in your `command.js` in commands folder:

### Example

{% tabs %}
{% tab title="command.js" %}
```javascript
module.exports = ({
name: "ping",
aliases: ['pong','info'],
code: `$pingms`
})
```
{% endtab %}
{% endtabs %}