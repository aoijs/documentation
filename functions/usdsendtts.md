---
description: Send a tts message.
---

# $sendTTS

This function lets the bot send a text-to-speech message with the given text in the current or given channel.

Raw usage: `$sendTTS[message; channelid ( optional)]`

#### Example Command:

```text
bot.command({
name: "tts",
code: `
$sendTTS[Hey guys, how are you?;827730677759082526]
`
})

// sends the tts message with given text to to the spam channel
```

