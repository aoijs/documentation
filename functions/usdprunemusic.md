# $pruneMusic

This function deletes the old message from onMusicStart\(\) to prevent flooding

```javascript
bot.command({
name: "play",
code: `$playSong[The Nights;5s;yes;Error]
$pruneMusic
`
})
```

