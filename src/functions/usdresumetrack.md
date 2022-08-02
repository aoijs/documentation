---
description: Resume, paused track.
---

# $resumeTrack

This function resumes a song after being paused.

### Usage

```php
$resumeTrack
```

### Example

```javascript
bot.command({
  name:"resume-track",
  code: `
  Resumed paused track!
  
  $resumeTrack
  `
  // Plays the track again on paused part.
});
```
