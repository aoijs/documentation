---
description: Shows how many users joined via custom url.
---

# $vanityUses

This function returns how many users joined through the vanity link.

> Your bot has to be in the given server.

### Usage

```php
$vanityUses[guildID?]
```

### Field

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| guildID? | the id of the server | number | no |

## Example

```javascript
bot.command({
  name: "vanity-uses",
  code: `Uses: $vanityUses`
})
```
