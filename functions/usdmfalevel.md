# $mfaLevel

Returns the guild mfa level \(true or false\)

#### Fields

1. Guild ID \(Optional\)

Raw usage: `$mfaLevel[Guild ID]`

#### Options

* Guild ID - Guild's mfa level you want to check.

#### Usage without optional field

```javascript
bot.command({
    name: "mfalevel",
    code: `$mfaLevel`
})
```

#### Usage with optional field

```javascript
bot.command({
    name: "mfalevel",
    code: `$mfaLevel[773352845738115102]`
}) // This will check the mfaLevel of Aoi.js official server
```

