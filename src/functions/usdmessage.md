---
description: 'Returns the message, from the Author.'
---

# $message

This function returns/repeats the author's message \(the content of the command's message\).

Raw usage: `$message[arg (optional)]`

#### Example Commands:

Without optional argument: If I do: `Hello Aoijs is awesome` behind the command the bot would return `Hello Aoijs is awesome`. 

```javascript
bot.command({
name: "say",
code: `
$message
`
})
```

With argument: If I do: `Hello Aoijs is awesome` behind my command the bot would return: `Aoijs` , because it's the second argument of my message.

```javascript
bot.command({
name: "say",
code: `
$message[2]
`
})
```

Getting the last argument \(last word\) of the message: `$message[last]` would return the last argument of the author's message.  If I do: `Hello Aoijs is awesome` behind my command the bot would return: `awesome` , because it's the lastargument of my message.

```javascript
bot.command({
name: "say",
code: `
$message[last]
`
})
```

