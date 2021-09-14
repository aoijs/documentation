---
description: Returns information about the song that is being played.
---

# $songInfo

#### Usage

```javascript
$songInfo[property;position]
```

#### Example usage for current playing song

```javascript
bot.command({
name: "songInfo",
code: `
Currrently Playing: $songInfo[title]
`
})
```

#### Example usage for next playing song

```javascript
bot.command({
name: "next-song",
code: `
Next Playing: $songInfo[title;1]
`
})
```

### Properties:

* title - Song Title
* description - Description of the song's YouTube video.
* duration - Duration of the song
* duration\_left - Duration left for the song to end.
* current\_duration - The current duration of the song.
* url - URL to the youtube video of the current song.
* userID - ID of the user that added the song.
* thumbnail - The thumbnail of the song.
* publisher - Channel that uploaded the song.
* publisher\_url - Link of the channel that uploaded the song.

{% hint style="info" %}
The current song's position is `0`- so next one's is `1` and so on.
{% endhint %}

