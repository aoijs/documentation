---
description: Adds blacklist error message
---

# $blacklistError

This function will show a blacklist error for given type.

### Usage 

```php
$blacklistError[type;error message]
```

### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| type | Type of the blacklist error | number | yes |
| error message | Error message that will be sending | number | yes |

## Example

```javascript
bot.command({
  name: "blacklist-error",
  code: `
  Yes, you're not blacklisted!
  
  $blacklistError[user;Hmm, it seems like you're blacklisted.]
  `
//If the author has been blacklisted, it will return the error.
});
```
