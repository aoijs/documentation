# $channelUsed

This function will show you the ID where the provided callback was triggered.

#### Usage

```javascript
bot.onMessageDelete();
bot.deletedCommand({
  channel: "channelID",
  code: `$username deleted a message in <#$channelUsed> 👀
  Content: $message`
});
```

