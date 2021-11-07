# $serverNames

This function returns all the names of the servers the bot is in.

#### Fields

This function has 1 optional field.

1. Separator \(Optional\)

Raw usage: `$serverNames[Separator (Optional)]`

#### Options

* Separator - Separator in between the server names.

#### Usage without optional field.

```javascript
bot.command({
    name: "servers",
    code: `Server names: $serverNames`
    //will return: serverName,serverName,serveName,etc
})
```

#### Usage with optional field.

```javascript
bot.command({
    name: "servers",
    code: `Server names: $serverNames[ / ]`
    // Will return: serverName / serverName / etc
})
```

