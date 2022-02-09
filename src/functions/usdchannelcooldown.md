---
description: Sets cooldown for current channel.

---

# $channelCooldown

This function sets a cooldown for the current channel

## Fields

1. time \(Required\)
2. error \(Required\)

#### Raw Usage: 
```php
$channelCooldown[time;error message]
```

## Options

* time - How long the cooldown will last
* error - The error message that will appear when the cooldown hasn't finished

## Usage

```javascript
bot.command({
name: "hello", 
code: `
Hello $username!
$channelCooldown[30s;This channel has a cooldown. \`%time%\ remains`
`
//%time% returns how long the cooldown remains for
})
```

