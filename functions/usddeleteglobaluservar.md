# $deleteGlobalUserVar

This function deletes the specified variable from the database

#### Fields

This function has 1 required field

1. Variable \(Required\)
2. User ID \(Optional\)

Raw Usage: `$deleteGlobalUserVar[variable;userID (optional)]`

#### Options

* Variable - The variable we're deleting
* User ID - The user we're deleting for

#### Usage

Without optional fields

```javascript
bot.command({
name: "deleteVar",
code: `$deleteGlobalUserVar[money]`
})
```

With optional fields

```javascript
bot.command({
name: "deleteVar",
code: `$deleteMessageVar[money;$mentioned[1]]`
})
```

