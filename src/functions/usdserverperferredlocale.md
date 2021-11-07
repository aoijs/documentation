# $serverPerferredLocale

This function returns the locale for the specified guild

#### Fields

This function has 1 optional field

1. Guild ID \(Required\)

Raw Usage: `$serverPerferredLocale[guildID (optional)]`

#### Options

* Guild ID - The guild we're getting the info from

#### Usage

Without the optional field

```javascript
bot.command({
name: "serverPerferredLocale",
code: `$serverPerferredLocale`
})
```

With optional field

```javascript
bot.command({
name: "serverPerferredLocale",
code: `$serverPerferredLocale[773352845738115102]`
})
```

