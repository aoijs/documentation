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

