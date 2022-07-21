---
description: Returns when the user joined the guild.
---

# $memberJoinedDate

This function returns when the user joined the current guild as ms.

### Usage

```php
$memberJoinedDate[guildID;userID]
```

### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| guildID | The ID of the guild | integer | yes |
| userID | The ID of the user | integer | no |

## Example

```javascript
bot.command({
  name: "joinndate",
  code: `
  $memberJoinedDate[$guildID;$authorID]
  `
  // Returns author's joined date as ms.
});
```
