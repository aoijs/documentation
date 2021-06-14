# $deleteChannelVar

This function deletes the specified variable from the database

#### Fields

This function has 1 required field

1. Variable \(Required\)
2. Channel ID \(Optional\)

Raw Usage: `$deleteChannelVar[variable;channelID (optional)]`

#### Options

* Variable - The variable we're deleting
* Channel ID - The channel we're deleting for

#### Usage

Without optional fields

```javascript
bot.command({
name: "deleteVar",
code: `$deleteChannelVar[delmsg]`
})
```

With optional fields

```javascript
bot.command({
name: "deleteVar",
code: `$deleteChannelVar[delmsg;827730677759082526]`
})
```

