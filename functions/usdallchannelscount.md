# $allChannelsCount

This function returns the amount of channels the bot has access to globally

#### Usage

This function has 1 optional field

1. Type \(Optional\)

Raw Usage: `$allChannelsCount[type (optional)]`

#### Types

* text
* voice
* category
* news

#### Usage

```javascript
bot.command({
name: "channelCount",
code: `
- $allChannelsCount Channels
- $allChannelsCount[category] Categories
- $allChannelsCount[text] Text Channels
- $allChannelsCount[voice] Voice Channels
- $allChannelsCount[news] Announcement Channels
`
})
```

