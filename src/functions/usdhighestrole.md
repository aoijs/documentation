---
description: 'Returns Highest Role Position ID, of the Author ID.'
---

# $highestRole

This function returns the user's highest positioned role ID.

### Usage
```php
$highestRole[userID?;guildID?;option?]
```


### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
|user ID|The id of the user whose role is to be returned|number|no|
| guild ID | The id of the guild | number | no |
| option | The option on basis of which the role will be returned | string | no |

#### Options
- `id` - Returns id of the role.
- `name` - Returns name of the role.
- `mention` - Returns the mention of the role.

## Example
```javascript
bot.command({
name: "role", 
code: `$highestRole[$authorID;$guildID;mention]`
})
```

