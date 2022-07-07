---
description: Returns username of the user.
---

# $username

This function returns the authors or given ID's Discord username.

### Usage

```php
$username[userID?]
```

### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| userID? | The ID of the specific user | number | no |

## Example

```javascript
bot.command({
  name: "username",
  code: `
  The \`285118390031351809\` is $username[285118390031351809].
  `
//Returns Neodevil
});
```
