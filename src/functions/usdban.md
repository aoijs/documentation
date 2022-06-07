---
description: Bans an user from the guild using their ID.
---

# $ban

This function allows you to ban someone from the server using their user ID.

### Usage

```php
$ban[userID;guildID (optional);MessagesToDelete (Optional);reason (Optional)]
```

### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| userID | The user the bot is banning | number | yes |
| guildID | The server ID where you are banning | number | yes |
| MessagesToDelete | How many of the messages over x days to delete of the banned user | number | no |
| reason | The reason in the audit logs | number | no |

## Examples

```javascript
bot.command({
  name: "ban",
  code: `
  $username[$message] has been banned from the guild.
  
  $ban[$message;$guildID;7;$noMentionMessage]
  
  $argsCheck[1;Just enter the User ID of who you want to ban.]
  `
});
```

```javascript
bot.command({
  name: "ban",
  code: `
  $username[$message] has been banned from the guild.
  
  $ban[$message;$guildID;7;$noMentionMessage]
  
  $argsCheck[1;Just enter the User ID of who you want to ban.]
  
  $onlyPerms[ban;Only cool people with ban perms can use this!]
    `
});
```
