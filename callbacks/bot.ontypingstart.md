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

