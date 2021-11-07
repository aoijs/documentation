# $serverAvailable

This function returns whether or not the specified server is available

#### Fields

This function has 1 optional field

1. Guild ID \(Required\)

Raw Usage: `$serverAvailable[guildID (optional)]`

#### Options

* Guild ID - The guild we're getting the info from

#### Usage

Without the optional field

```javascript
bot.command({
name: "serverAvailable",
code: `$serverAvailable`
})
```

With optional field

```javascript
bot.command({
name: "serverAvailable",
code: `$serverAvailable[773352845738115102]`
})
```

