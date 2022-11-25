---
description: Pause playing track.
---

# $pauseTrack

You can pause playing track with this function.

### Usage 

```php
$pauseTrack
```

### Example

```javascript
bot.command({
  name: "pause-track", 
  code: `
  Paused the track.
  
  $pauseTrack
  `
  // Paused playing track in the voice/stage channel
});
```
