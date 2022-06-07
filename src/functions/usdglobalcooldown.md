---
description: 'Set a Global cooldown, with all Guilds'
---

# $globalCooldown

This function is used to set a global cooldown for all servers.

## Fields
This function has 2 fields

- Time (Required)
- Error (Optional)

## Usage
```php
$globalCooldown[time;error when cooldown activated?]
```

## Options
- Time - The time until which the cooldown will last
- Error - The error to be displayed when cooldown is active.

{% hint style="info" %}
You can use %time% to return the remaining cooldown time.
{% endhint %}

## Example

```javascript
bot.command({
name: "hello", 
code: `
$description[Hello!]
$globalCooldown[1m;Hey, you need to wait %time%!]
}) // Returns the time until which you need to wait to execute the command
```

