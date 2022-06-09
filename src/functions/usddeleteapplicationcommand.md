---
description: Delete an application command.
---

# $deleteApplicationCommand

Delete an application command which is can be:
* Slash type
* Message type
* User type

### Usage

```php
$deleteApplicationCommand[guildID/global;application id]
```

### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| guildID/global | The field, which we're going to delete on `guild` or `global` | str & num | yes |
| application id | The application command that we're going to delete | number | yes |

## Examples

* Deleting on a server

```javascript
bot.command({
  name: "delete-application-command",
  code: `
  $deleteApplicationCommand[$guildID;$getApplicationCommandID[help;$guildID]]
  
  Deleted help command, since it was unnecessary...
  `
});
```

* Deleting global application command

```javascript
bot.command({
  name: "delete-application-command",
  code: `
  $deleteApplicationCommand[global;$getApplicationCommandID[help;global]]
  
  Deleted help command, since it was unnecessary...
  `
});
```
