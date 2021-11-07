# $serverSplash

This function returns server splash url. Server Splash is the invite background image

```text
$serverSplash[guildID;size (optional)]
```

```javascript
bot.command({
name: "serverSplash",
code: `$image[$serverSplash[$guildID;2048]]`
})
```

