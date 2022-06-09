---
description: Returns amount of banned users.
---

# $banCount

`$banCount` returns how many bans the current guild has, _lets hope its not thay much hehe!_

### Usage

```php
$banCount[guild id?]
```

### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| guild id? | Returns amount of bans in the given guild id | number | no |

## Example

```javascript
bot.command({
  name: "ban-count",
  code: `
  $username: How many members got ban?
  
  $username[$clientID]: $banCount[697039582922801182] members!
  `
// Returns 13 
});
```

