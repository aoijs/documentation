---
description : Sets a cooldown for the current channel.
---

# $channelCooldown

This function sets a cooldown for the current channel.

### Usage 
```php
$channelCooldown[time;error?]
```

### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| time | How long the time will last | alphanumeric | yes |
| error | The error message that will appear when the cooldown hasn't finished | string | no |


## Example

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

