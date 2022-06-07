---
description: Forces the bot to leave the specified / current server.
---

# $botLeave

This function makes the bot leave the current / specified server.

## Fields

This function has 1 optional field

1. Server ID \(Optional\)

### Usage 
```php
$botLeave[serverID (optional)]
```

## Options

* Server ID - The server of which the bot is going to leave from

{% hint style="danger" %}
Using this function will make your bot leave the specified server, we recommend using [$onlyForIDs](./usdonlyforids.md) function to limit the usage of this function to the owners of the bot.
{% endhint %}

## Example

- Without optional fields

```javascript
bot.command({
    name: "exit",
    code: `
    $botLeave
    $onlyForIDs[278342221202194434;You're not Chiwi!]
    `
});

// I just used my ID but you can replace it with yours.
```

- With optional fields

```javascript
bot.command({
    name: "exit",
    code: `
    $botLeave[773352845738115102]
    $onlyForIDs[278342221202194434;You're not Chiwi!]
    `
});

// I just used my ID but you can replace it with yours.
// I just used Akarui Development server's id for example.
// You can specify the guild ID of the server from which your bot will leave the server.
```



