---
description: Changes volume for current playing song.
---

# $volume

This function can change the volume of the current playing song. The minimum number is 0 and the highest number is what ever you want~

### Usage

```php
$volume[volume of audio?]
```

### Field

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| volume of audio? | for increasing the playing audio's volume | number | no |


###### Footnote

> _volume function itself returns the volume!_

## Example

```javascript
bot.command({
  name: "volume",
  code: `
  $volume[50]
  `
});
 // Sets the volume to 50%
```
