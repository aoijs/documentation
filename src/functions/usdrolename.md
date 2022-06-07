---
description: Returns a Role name using their ID
---

# $roleName

This function returns the name of the specified role ID.

## Fields
This function has 1 required field

- Role ID (Optional)

### Usage
```php
$roleName[role ID]
```

## Option
- Role ID - The role id of the role whose name is to be displayed.

## Example

```javascript
bot.command({
name: "roleinfo", 
code: `
Role name: $roleName[$mentionedRoles[1]]
Role ID: $mentionedRoles[1]` 
})
```

