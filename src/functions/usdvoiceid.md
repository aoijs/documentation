---
description: Returns the current voice channel ID the user is in
---

# $voiceID

This function simply returns the voice channel ID that the user is in

Heres the usage:

```text
$voiceID[userID (optional)]
```

Now lets find the voice ID of the author

```javascript
bot.command({
name: "voiceID",
code: `
$voiceID
`
})
```

And let's find the voice ID of Kubaturi

```javascript
bot.command({
name: "voiceID",
code: `
$voiceID[$findUser[Kubaturi]]
`
})
```

As always you can use `$voiceID[$message]`

