---
description: Returns channel ID for specified channel
---

# $findServerChannel

This function finds and returns the id of the specified channel in the current guild. Yes/No will determine if function returns current channel id \(yes\) or undefined \(no\) if no match was found. Default is yes

#### Fields

This function has 1 required field

1. Server Channel \(Required\)
2. Return Current Channel ID \(Optional\)

Raw Usage: `$findChannel[server channel;returnCurrentChannel (yes/no) (optional)]`

#### Options

* Server Channel - The channel we're finding. You can use name/id/mention
* Return Current Channel ID - Returns current channel id if no channel found

#### Usage

```javascript
bot.command({
name: "server-channel",
code: `$findServerChannel[announcements]`
})
```

