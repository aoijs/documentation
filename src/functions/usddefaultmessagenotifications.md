---
description: Return the guild default message notification level.
---

# $defaultMessageNotification

This function returns the level of a server's default message notifications.

> Returns either `Mentions` or `All`.

### Usage

```php
$defaultMessageNotification[guildID?]
```

### Property

| FIELD | TYPE | DESCRIPTION |
| ----- | ----- | ----- | 
| guildID? | integer | The guild id | 

## Example

```javascript
bot.command({
  name: "default-message-notification",
  code: `
  Notifications type of the server $serverName[773352845738115102]: $defaultMessageNotification[773352845738115102]
  `
});
```
