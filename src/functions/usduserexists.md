---
description: Checks if the given user ID exists.
---

# $userExists

This function checks if the given user ID exists in discord.

```php
$userExists[userID]
```

### Field

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| user ID | The user's ID | number | yes |

```javascript
bot.command({
	name: "user-exists",
	code: `
	Does 285118390031351809 exist? $userExists[285118390031351809]
	`
// Returns true
});
```

