---
description: Returns when the user joined the guild.
---

# $memberJoinedDate

This function returns when the user joined the current guild as ms.

### Usage

```php
$memberJoinedDate[userID?;guildID?]
```

### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| userID? | The ID of the guild | integer | no |
| guildID? | The ID of the user | integer | no |

## Example

```javascript
bot.command({
  name: "member-joined-date",
  code: `
  $memberJoinedDate[$authorID;$guildID]
  `
/*
  Returns author's joined date as ms. 
  Also without parameters it would still return author's joined date for the guild.
*/
});
```
