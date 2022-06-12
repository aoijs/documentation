---
description: Used to delete the specified invite.
---

# $deleteInvite

`$deleteInvite` allowing you to delete invite of the specified invite code.

### Usage

```php
$deleteInvite[code;guildID?;reason]
```

### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| code | The invite code to be deleted | alphanumeric | yes |
| guild ID | The ID of the guild | number | no |
|reason |The reason why you want to delete the link|string|yes|

## Examples

```javascript
bot.command({
  name: "delete",
  code: `
  $deleteInvite[$message;$guildID;I want to delete this invite!]
  `
});
```
