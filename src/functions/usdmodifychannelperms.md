---
description: Modifies a channel's permissions to the given permissions.
---

# $modifyChannelPerms

This function edit's the specified channel's permission for given role ID or user ID.[^1]

  [^1]: For changing **@everyone** role's permission, you can use `$guildID` on roleID parameter.

### Usage 

```php
$modifyChannelPerms[roleID/userID;channelID; perms...]
```

### Properties

| FIELD | TYPE | DESCRIPTION |
| ----- | ----- | ----- | 
| roleID/userID | integer | The ID of the role/user | 
| channelID | integer | The ID of the channel |
| perms... | string | The perms will be changed for the channel |

#### Permission Operators

We have three permission operators for Discord channels:

* `+` — Allowed
* `\` — Default (role based)
* `-` — Disallowed

## Example

```javascript
bot.command({
  name: "modify-channel-perms",
  code: `
  Oops! You just took off your permission to chat in this channel!
  
  $modifyChannelPerms[$authorID;$channelID;-sendmessages]
  `
});
```
