# $joinVC

Makes the bot join an specified voice channel.

#### Fields

This function has 1 required field.

1. Channel ID \(Required\)

Raw usage: `$joinVC[Channel ID]`

#### Options

* Channel ID - Channel where the bot should connect to.

#### Usage

```javascript
bot.command({
    name: "",
    code: `Joined!
    $joinVC[816751491451977768]` 
})

/**
 * This would make the bot join the #Staff VC
 * Located in the official aoi.js server.
**/
```

