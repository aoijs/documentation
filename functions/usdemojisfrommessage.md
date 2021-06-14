# $emojisFromMessage

This function filters out all emojis from the provided message and returns

```text
$emojisFromMessage[message;separator (optional)]
```

```javascript
bot.command({
name: "emojis", 
code: `
Emojis:
$emojisFromMessage[Hello😀, Made with ❤️]
`
//Will return: 😀,❤️
})
```

