---
description : Used to set a position to the specified role.
---

# $setRolePosition
This function is used to set a position to the specified role.

## Fields
- role ID (Required)
- new Position (Required)
- guild ID (Optional)

### Raw Usage
`$setRolePosition[roleID;newPosition;guildID?]`

## Options
- Role ID - The id of role whose position is to be changed.
- New Position - The new position of the role to be assigned. The position must be in integer.
- Guild ID - The id of the guild.

### Usage

- Without optional fields:-

```js
bot.command({
name: "new-position",
code: `$setRolePosition[$mentionedRoles[1];$noMentionMessage]`
}) // Changes position of mentioned role in the guild.
```

- Without optional fields:-

```js
bot.command({
name: "new-position",
code: `$setRolePosition[$mentionedRoles[1];$noMentionMessage;773352845738115102]`
}) // Changes position of mentioned role in Akarui Development server.
```
