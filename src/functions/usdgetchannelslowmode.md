# $getChannelSlowmode

This function gets the specified channels slowmode

#### Fields

This function has 1 optional field

1. Channel ID \(Optional\)

Raw Usage: `$getChannelSlowmode[channelID (optional)]`

#### Options

* Channel ID - The channel we're getting the slowmode from

#### Usage

Slowmode for the current channel

```javascript
bot.command({
name: "get-slowmode",
code: `
Current Slowmode: $getChannelSlowmode
`
```

Slowmode for the mentioned channel

```javascript
bot.command({
name: "get-slowmode",
code: `
Slowmode: $getChannelSlowmode[$mentionedChannels[1]]
`
```

