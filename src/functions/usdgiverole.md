---
description: Give a role to an user.
---

# $giveRole

This function gives a role to the specified user. This is generally faster than [$giveRoles](usdgiveroles.md).

```php
$giveRole[guildID;userID;roleID]
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
  name: "give-role",
  code: `
  $giveRole[$guildID;$authorID;797332449314734141]
  `
});
```
