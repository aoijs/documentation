---
description: Skip the current track to next queue song.
---

# $skip

This function skips to the next track in the queue.

### Usage

```php
$skip
```

### Example

```javascript
bot.command({
  name: "skip",
  code: `
  Skipped current track.
  
  $skip
  `
  // Skips the current track.
});
```
