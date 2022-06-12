---
description: Returns the ID\(s\) of the bot's owners.
---

# $botOwnerID

This function returns the ID\(s\) of the bot's owners.

### Usage 
```php
$botOwnerID[separator?]
```

### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| separator | The symbol/letter that separates the 2 or more ids | alphanumeric | no |


## Examples

```javascript
bot.command({
name: "botOwner",
code: `Here are my owners: $botOwnerID`
//Separator is for if your bot has multiple owners
})
```

