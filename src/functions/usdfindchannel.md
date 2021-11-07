---
description: 'Retrieve the Channel ID, when writing the name of the Channel. (Global)'
---

# $findChannel

This function returns the channel ID of the specified channel. Yes/No will determine if function returns current channel id \(yes\) or undefined \(no\) if no match was found. Default is yes

#### Fields

This function has 1 required field

1. Channel \(Required\)
2. Return Current Channel ID \(Optional\)

Raw Usage: `$findChannel[channel;returnCurrentChannel (yes/no) (optional)]`

#### Options

* Channel - The channel we're finding. You can use name/id/mention
* Return Current Channel ID - Returns current channel id if no channel found

#### Usage

```javascript
bot.command({
name: "channel",
code: `$findChannel[rubens-basement]`
})
```

