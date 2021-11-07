# $deleteServerVar

This function deletes the specified variable from the database

## Fields

This function has 1 required field

1. Variable \(Required\)
2. Server ID \(Optional\)

Raw Usage: `$deleteServerVar[variable;serverID (optional)]`

## Options

* Variable - The variable we're deleting
* Server ID - The server we're deleting for

## Usage

Without optional fields

```javascript
bot.command({
name: "deleteVar",
code: `$deleteServerVar[total_money]`
})
```

With optional fields

```javascript
bot.command({
name: "deleteVar",
code: `$deleteServerVar[total_money;773352845738115102]`
})
```

