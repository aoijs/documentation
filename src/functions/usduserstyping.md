# $usersTyping

This function returns all the users who are typing in the specified channel

```
$usersTyping[channelID;username/mention/tag;separator (optional)]
```

```javascript
bot.command({
name: "usersTyping",
code: `Users who are typing: $usersTyping[$channelID;username;/]
`
})
```

![This is what this function would grab](<../../.gitbook/assets/image (16).png>)
