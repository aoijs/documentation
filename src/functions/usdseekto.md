# $seekTo

This function seeks to a the specified duration of the song

```text
$seekTo[seconds]
```

```javascript
bot.command({
name: "seek",
code: `
$seekTo[5]
`
//This skips to the 5 second mark of the song
//$skipTo[50] would skip to the 50 second mark of the song
})
```

Seek with user input

```javascript
bot.command({
name: "seek",
code: `
$seekTo[$message]
`
//Usage - !seek 28
//This would seek to the 28 mark of the song
})
```

