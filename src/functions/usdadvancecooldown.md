---
description: The cooldown function, but advanced version.
---

# $advanceCooldown

This function will create a cooldown for the given ID.

### Usage 

```php
$advanceCooldown[time;id;error?]
```

### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| time | The cooldown time | string | yes |
| id | The ID of the cooldown will create for | number | yes |
| error message? | The error message | string | no |

#### Suffixes

* `s` - Seconds
* `m` - Minutes
* `h` - Hours
* `d` - Days
* `w` - Weeks

## Example

```javascript
bot.command({
  name: "advance-cooldown",
  code: `
  Hello, World!
  
  $advanceCooldown[15s;$guildID;Wait %time% seconds before using this command again.]
  `
});
```
