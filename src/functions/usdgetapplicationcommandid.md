---
description: Get application command ID.
---

# $getApplicationCommandID

Get an application command which is can be:
* Slash type
* Message type
* User type

### Usage

```php
$getApplicationCommand[application name;location]
```

### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| application id | The application command that we're going to delete | number | yes |
| location | The field, which we're going to delete on `guild` or `global` | str & num | yes |

#### Location Types

* `guildID` — Specific server id
* `global` — Global application commands as it's name

## Examples

* Getting application command's ID from a server

```javascript
bot.command({
  name: "get-application-command-id",
  code: `
  $getApplicationCommandID[ban;$guildID]]
  `
});
```

* Getting global application command's ID

```javascript
bot.command({
  name: "get-application-command-id-g",
  code: `
  $getApplicationCommandID[help;global]
  `
});
```
