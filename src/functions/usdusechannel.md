---
description: Sends message to specified channel
---

# $useChannel

This function sends a message to the given channel

```php
$useChannel[channel ID]
```

## Example

```javascript
bot.command({
name: "useChannel",
code: `Hi!
$useChannel[773363417338609674]` //Sends 'Hi!' in the given channel
})
```

{% hint style="info" %} Make sure that $useChannel is below the message or embed that you want to send since aoi.js reads code from bottom to top. {% endhint %}

