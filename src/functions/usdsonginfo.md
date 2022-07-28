---
description: Returns given track's info.
---

# $songInfo

This function returns the property of the given position's track.

### Usage

```php
$songInfo[response?;position?]
```

### Properties

| FIELD | TYPE | DESCRIPTION |
| ----- | ----- | ----- | 
| response? | string | The property of track's info | 
| position? | integer | Position of the track |

#### Response Properties

* `title` — Returns track's title
* `description` — Returns description of the track
* `url` — Returns URL of the track
* `thumbnail` — Returns thumbnail of the current track[^1]
* `duration` — Returns duration of the track
* `identifier` — Returns the track's platform
* `author` — Returns publisher's name
* `authorURL` — Returns publisher's url
* `likes` — Returns likes of the track
* `views` — Returns views of the track[^2]
* `createdTimestamp` — Returns the track's published time

  [^1]: Some tracks might now have an album cover.
  
  [^2]: You might not able to see views on some platforms.
  
## Song Info Examples

* Without optional properties

```javascript
bot.command({
  name: "song-info",
  code: `
  $songInfo
  `
  // Returns current playing track's title.
});
```

* With optional properties

```javascript
bot.command({
  name: "song-info",
  code: `
  $songInfo[author;1]
  `
  // Returns the publisher's name of the next song.
});
```
