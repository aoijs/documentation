---
description: Returns the ping of the message in ms.
---

# $messagePing

This function returns the message latency in Milliseconds.

### Usage
```php
$messagePing
```

## Examples

```javascript
bot.command({
name: "messageping", 
code: `
Message Latency: $messagePing ms`
})
```

