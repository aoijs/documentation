---
description: Used to add perms to the application command 
---

# $addApplicationCommandPermissions
Used to add specific permissions to the existing permissions to particular application command in the specified guild.

## Types
- Guild ID (Optional)
- Application ID (Required)
- Permissions (Required)

### Raw Usage
`$addApplicationCommandPermissions[guildId?;id;$authorID/$roleID[example]:USER/ROLE:yes/no]`

## Options
* Guild ID - The guild in which the application command is to be modified.
* Application ID - The id of the application command that is to be modified.
* Permissions - The perms that is to be given.

## Usage

- With authorID

```js
bot.command({
    name: "update",
    code: `$addApplicationCommandPermissions[$guildID;$getApplicationCommandID[aoijs;$guildID];$authorID:USER:yes]`
});
```

- With roleID

```js
bot.command({
    name: "update",
    code: `$addApplicationCommandPermissions[$guildID;$getApplicationCommandID[aoijs;$guildID];$roleID[example]:ROLE:yes]`
});
```