---
description: Change role's permissions.
---

# $modifyRolePerms

This function allows the bot to modify the given role is permissions

### Usage

```php
$modifyRolePerms[guildID;roleID;perms...]
```

### Properties

| FIELD | TYPE | DESCRIPTION |
| ----- | ----- | ----- | 
| guildID | integer | The ID of the server | 
| roleID | integer | The ID of the role |
| perms... | string | The permissions going to be changed on the role. |


#### Permission Operators

We have two permission operators for Discord Roles[^1]:

* `+` — Allow
* `-` — Disallow

  [^1]: You can also use `+all` or `-all` on permission parameter to enable or disable **all the permissions**.

## Examples 

* Allowing a permission:

```javascript
bot.command({
  name: "modifyRolePerms",
  code: `
  $modifyRolePerms[36732971190973292;+admin]
  `
});
```

* Denying a permission:

```javascript
bot.command({
  name: "modifyRolePerms",
  code: `
  $modifyRolePerms[36732971190973292;-admin]
  `
});
```

* Allowing all permissions:

```javascript
bot.command({
  name: "modifyRolePerms",
  code: `
  $modifyRolePerms[36732971190973292;+all]
  `
});
```

