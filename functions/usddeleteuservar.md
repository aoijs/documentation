# $deleteUserVar

This function deletes the specified variable from the database

#### Fields

This function has 1 required field

1. Variable \(Required\)
2. User ID \(Optional\)
3. Guild ID \(Optional\)

Raw Usage: `$deleteUserVar[variable;userID (optional);guildID (optional)]`

#### Options

* Variable - The variable we're deleting
* User ID - The user we're deleting for
* Guild ID - The guild where the user is

#### Usage

Without optional fields

```javascript
bot.command({
name: "deleteVar",
code: `$deleteUserVar[money]`
})
```

With optional fields

```javascript
bot.command({
name: "deleteVar",
code: `$deleteUserVar[money;$mentioned[1]]`
})
```

