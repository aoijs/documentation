---
description: This function returns the error that the interpreter threw.
---

# $error

With this function you can execute a command if a command execution failed becasue of an interpreter error. The bot will execute the error property of the command if the intepreter throws an error. $error returns that error that was sent in the bot's console.

#### Usage

Example usage of the `error` property with the usage of $error inside to send the console error of the eval command in the given channel \($channelSendMessage\). You can use basically all functions in there.

```javascript
bot.command({
name: "eval",
error: `$channelSendMessage[839061638707019836;$userTag had a problem: $error in $channelName!]`
code: `
$djsEval[message]
`
})
```

![Example message of the error log.](../.gitbook/assets/image%20%283%29.png)

