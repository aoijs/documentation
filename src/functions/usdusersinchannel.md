---
description: Returns the users that are connected to the current voice channel that the bot is in.
---

# $usersInChannel

This function returns the users that are in the given voice channel.

### Usage

```php
$usersInChannel[voiceChannelID;option?;separator?]
```

### Field

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| voiceChannelID | The ID of the voice channel | number | yes |
| option? | The option of the returning user's | string | no |
| seperator? | Seperator of userIDs | string | no |

#### Option Types

* `id` — Returns ID of the users with the given role
* `user.username` — Returns name of the users with the given role
* `nickname` — Returns nickname of the users with the given role
* `mention` — Returns the users with mentioning from given role

## Example

* Using this without given parameters

```javascript
bot.command({
  name: "usersInChannel",
  code: `
  $usersInChannel[$voiceID;nickname;, ]
  `
// Will return: Neo the Daddy, Kal'tsit
});
```
