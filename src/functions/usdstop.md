---
description: Stops the bot from playing tracks.
---

# $stop

This function makes the queue list empty and skip all the tracks. 

### Usage

```php
$stop
```

### Example

```javascript
bot.command({
  name: "stop",
  code: `
  Stopped playing track.
  
  $stop
  `
  // Stops playing tracks.
});
```
