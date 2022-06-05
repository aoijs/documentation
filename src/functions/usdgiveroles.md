---
description: Give roles to an user.
---

# $giveRoles

This function gives roles to the specified user.

```php
$giveRoles[guildID;userID;roleID;roleID;...]
```

#### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| guildID | The server ID of the role | integer | yes |
| userID | The user ID, which will be taking the role | integer | yes |
| roleID | The ID of the role will be given to user | integer | yes |

###### Footnote
* Be sure bot's role higher than the role it will give!

```javascript
bot.command({
  name: "give-roles",
  code: `
  $giveRole[$guildID;$authorID;797332449314734141;12345678987654321]
  `
});
```
