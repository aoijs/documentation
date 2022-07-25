---
description: Disables mentions.
---

# $disableMentionType

This function removes any mention for specific type.

### Usage

```php
$disableMentionType[type]
```

### Property

| FIELD | TYPE | DESCRIPTION |
| ----- | ----- | ----- | 
| type | string | The type for disabling mention | 

### Property Types

* `all` — Disables mentions for all type of the mentions
* `everyone` — Disables mentions for *@everyone* and *@here* type mentions
* `roles` — Disables mentions for roles
* `users` — Disables mentions for users

## Example

```javascript
bot.command({
  name: "disable-mention-type", 
  code: `
  $message
  
  $disableMentionType[all]
  `
  // client won't able to mention anyone 
});
```
