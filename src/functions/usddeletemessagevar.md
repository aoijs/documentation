# $deleteMessageVar

This function deletes the specified variable from the database

#### Fields

This function has 1 required field

1. Variable \(Required\)
2. Message ID \(Optional\)

Raw Usage: `$deleteMessageVar[variable;messageID (optional)]`

#### Options

* Variable - The variable we're deleting
* Message ID - The message we're deleting for

#### Usage

Without optional fields

```javascript
bot.command({
name: "deleteVar",
code: `$deleteMessageVar[author]`
})
```

With optional fields

```javascript
bot.command({
name: "deleteVar",
code: `$deleteMessageVar[author;829166243935682582]`
})
```

