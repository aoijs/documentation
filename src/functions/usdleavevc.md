---
description: Makes the bot leave the voice channel where it is connected
---
# $leaveVC

Makes the bot leave the voice channel where it is connected, if any.

### Usage
```php
$leaveVC
```
## Example

```javascript
bot.command({
    name: "leave",
    code: `I left the VC!
    $leaveVC`
})
```

