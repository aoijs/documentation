---
description: Changes the color of the specified role's ID
---

# $setRoleColor

This function changes the color of a role

### Usage 
```php
$setRoleColor[roleID;hex/int_color]
```

### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| role ID | The id of the role whose colour is to be changed | number | yes |
| color |The color we're changing to|hex/int color|yes|

## Example

```javascript
bot.command({
name: "crole",
code: `Changed the role's color to #FF0000
$setRoleColor[$mentionedRoles;FF0000]`
})
```

