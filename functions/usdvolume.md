---
description: Changes volume for current playing song
---

# $volume

This function can change the volume of the current playing song. The minimum number is 0 and the highest number is what ever you want \(Just be careful as it can cause earrape\)

Function Usage: 

```text
$volume[number]
```

Using it in a command:

```javascript
bot.command({
name: "volume",
code: `
$volume[50]
`
})
 // Sets the volume to 50%
```

You can also set the volume by user inputs by using [$message](usdmessage.md)

```javascript
bot.command({
name: "volume",
code: `
$volume[$message]
`
})
 // Sets the volume to what ever the user inputs
```

To see the current volume, just have $volume

