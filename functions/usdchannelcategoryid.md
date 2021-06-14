---
description: Returns the channel category ID
---

# $channelCategoryID

This function will display the category ID the current/specified channel is in

#### Fields

This function has 1 optional field

1. Channel ID \(Optional\)

Raw Usage: `$channelCategoryID[channel ID (Optional)]`

#### Options

* Channel ID - The channel of which we are getting the category id from

#### Usage

```javascript
bot.command({
    name: "categoryID",
    code: `$channelCategoryID[772414449839636490]` //Returns 772414329206734899
})
```

