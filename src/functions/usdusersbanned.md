---
description: Returns a list of users that are banned from current guild.
---

# $usersBanned

This function returns the list of banned users from the current server with optional seperator sorted by userID/mention or usernames. Default return are usernames of the banned users.

> If your server has many bans, use functions like [$cropText](usdcroptext.md) to stop after 2,000 chars or [$createFile](usdcreatefile.md) to send the full list in a text file.

### Usage

```php
$usersBanned[guildID?;force?;options?;separator?]
```

### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| guildID? | The ID of the server | number | no |
| force? | Forcing to fetch banned users | boolean | no |
| option? | The option of the returning user's | string | no |
| seperator? | Seperator of userIDs | string | no |

#### Option Types

* `id` — Returns ID of the users
* `username` — Returns name of the users

## Example

```javascript
bot.command({
  name: "users-banened",
  code: `
  List of banned users:
  $usersBanned[$guildID;yes;username;, ]
  `
// Returns all banned users sorted by their username separated by a comma.
});
```
