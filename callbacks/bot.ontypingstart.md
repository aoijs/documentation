---
description: >-
  An event that gets executed, if the bot sees someone typing in a text channel.
  To let the bot listen to the event, add one bot.onTypingStart() callback
  inside your mainfile.
---

# bot.onTypingStart

This callback will trigger when the bot sees someone typing.

Example:

#### Usage:

```javascript
bot.typingStartCommand({
channel: "ID", // (Optional)
code: `Your code`
});
```

#### Example Command:

```javascript
bot.typingStartCommand({
channel: "836582026139664414",
code: `Hey! I see, you're typing? 👀
`
});
```

#### Command Handler Usage:
For people who use `bot.loadCommands()` handler.
```javascript
module.exports = ({
channel: "ID",
code: `
code here
`,
type: 'typingStartCommand'
})
```
#### Example command:

```javascript
module.exports = ({
channel: "705681477169315863",
code: `
Hey! I see, you're typing? 👀
`,
type: 'typingStartCommand'
})
```
