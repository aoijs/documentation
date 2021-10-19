# $clearSongQueue

With this function you can clear the song queue completely but let the bot finish the current song before ending the music playback so queue will be purged but current song won't stop the playback.

#### Example Usage:

```js
bot.command({
name: "clear-queue",
code: `
I cleared the song queue and stop the music playback after the current song!
$clearSongQueue
`
})
```

