---
description: Check if the user is boosting.
---

# $isBoosting

This function checks if the given user is boosting or not. Returns boolean.

### Usage

```php
$isBoosting[userID?;guildID?]
```

### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| userID | The id of the user whose boosting status has to be checked | number | no |
| guildID | The id of the guild | number | no |

## Example
- Without optional field

```javascript
bot.command({
name: "isboost", 
code: `$isBoosting`
})
```

- With optional field

```javascript
bot.command({
name: "isboost", 
code: `$isBoosting[$userID[Ayaka];$guildID[Akarui Development]]`
})
```

