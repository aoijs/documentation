# $joinVC

Makes the bot join an specified voice channel.

#### Fields

This function has 1 required field.

1. Channel ID \(Required\)
2. Join As Speaker \(Optional\)

Raw usage: `$joinVC[Channel ID;Join As Speaker?]`

#### Options

* Channel ID - Channel where the bot should connect to.
* Join As Speaker - If you want the bot to join as speaker. \(default value: yes\)

#### Usage

```javascript
bot.command({
    name: "",
    code: `Joined!
    $joinVC[816751491451977768;yes]` 
})

/**
 * This would make the bot join the #Staff VC
 * Located in the official aoi.js server.
**/
```

