---
description: A command that gets executed in an interval as a loop.
---

# bot.loopCommand

This command loops a code to run every x **milliseconds.**

Properties are `code`, `every`, `executeOnStartup` and `channel` .

The properties `channel` and `executeOnStartup` are optional.

## Usage:

```javascript
bot.loopCommand({
code: `
...
`,
channel: "channel id",
executeOnStartup: true/false,
every: ms
})
```

## Example command:

```javascript
bot.loopCommand({
code: `
hi
`,
channel: "804505461076131840",
executeOnStartup: true,
every: 300000
})

/*
This command will send 'hi' to the given channel id every 5 minutes. 
ExecuteOnStartup means when the bot starts/comes online, the loop will start
*/
```

{% hint style="warning" %}
Keep in mind that `every` property is in ms! Watch out not to rate limit your bot!
{% endhint %}

