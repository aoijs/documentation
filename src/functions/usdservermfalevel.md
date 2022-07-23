---
description: Check given guild is mfa level. 
---

# $serverMFALevel

Returns guild is mfa level.

### Usage

```php
$serverMFALevel[guildID?]
```

### Properties

| FIELD | TYPE | DESCRIPTION |
| ----- | ----- | ----- | 
| guildID? | integer | Guild's mfa level we want to check |

## Example

```javascript
bot.command({
  name: "server-mfa-level",
  code: `
  $mfaLevel[$guildID]
  `
  // This will check the mfa level of current server and returns boolean.
});
```
