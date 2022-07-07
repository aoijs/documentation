---
description: Returns an user ID with given username.
---

# $userID

This function returns the user ID of the given username.

### Usage

```php
$userID[username]
```

### Field

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| username | The user's username | string | yes |

## Example

```javascript
bot.command({
  name: "userid",
  code: `
  $userID[Neodevil]
  ` 
//Returns 285118390031351809
});
```
