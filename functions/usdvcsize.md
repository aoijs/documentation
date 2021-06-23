---
description: Returns the size of the provided type in Provided guild or global
---

# $vcSize

This function simply returns the size of the provided type in Provided guild or global

Here is the usage:

```text
$vcSize[channels/users/songs;guildID/all (optional)]
```

Now lets find the size of voice size requested

```javascript
bot.command({
name: "vcSize",
code: `
$vcSize[channels;all]
`
})
```

And let's find the voice channel's size of the channel where you are listening to the bot

```javascript
bot.command({
name: "vcSize",
code: `
$vcSize[users;$guildID]
`
})
```

