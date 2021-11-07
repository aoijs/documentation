---
description: Returns the Client Latency ms.
---

# $botPing

This function returns the client latency in Milliseconds.

Example response: 64 \(for 64 ms\)

```javascript
bot.command({
name: "botping", 
code: `
Latency: $botPing ms`
})
```

