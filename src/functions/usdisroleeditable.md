# $isRoleEditable

This function checks if the role can be edited. Returns boolean.

## Fields
- Role ID (Required)
- Guild ID (Optional)

### Raw Usage
`$isRoleEditable[roleID;guildID?]`

## Options
- Role ID - The id of the role to be edited.
- Guild ID - The id of the guild.

### Usage
- Without optional fields:-

```js
bot.command({
name: "is-editable",
code: `$isRoleEditable[$roleID[Staff]]`
}) // Returns boolean
```

- With optional fields:-

```js
bot.command({
name: "is-editable",
code: `$isRoleEditable[$roleID[Staff];773352845738115102]`
}) // Returns boolean
```
