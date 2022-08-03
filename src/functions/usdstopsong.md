---
description: Stops the bot from playing songs.
---

# $stop

This function makes the queue list empty and skip all the songs. 

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
