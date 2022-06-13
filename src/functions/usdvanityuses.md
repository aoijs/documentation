---
description: Shows how many users joined via custom url.
---

# $vanityUses

This function returns how many users joined through the vanity link[^1]

### Usage

```php
$vanityUses[guild id?]
```

### Field

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| guild id? | the id of the server | number | no |

## Example

```javascript
bot.command({
  name: "vanityUses",
  code: `Uses: $vanityUses`
})
```

[^1]: Your bot has to be in the given server.
