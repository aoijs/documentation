---
description: Bans an user from the guild using their ID.
---

# $ban

`$ban` allows you to ban someone from the server using their user ID. 

### Usage

```php
$ban[guildID;userID;days?;reason]
```

### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| guild id | The server ID where the user will get ban | number | yes |
| user id | The user the bot is banning | number | yes |
| days | How many of the messages over x days to delete of the banned user | number | no |
| reason | The reason in the audit logs | string | yes |

###### Footnote

> *Do not forget to use `$onlyBotPerms` and `$onlyPerms` to detect user has permission for this action, either bot!*


## Examples

```javascript
bot.command({
  name: "ban",
  code: `
  $username[$mentioned] has been banned from the guild.
  
  $ban[$guildID;$mentioned;7;$noMentionMessage]
  `
// Deleted 7 days of messages the user
// 💡 That's also called as "soft-ban"
});
```

* Without deleting user's messages on the guild:

```javascript
bot.command({
  name: "ban",
  code: `
  $username[$message] has been banned from the guild.
  
  $ban[$guildID;$message;0;$noMentionMessage]
  `
// Didn't delete any messages of the user, but banned
});
```

