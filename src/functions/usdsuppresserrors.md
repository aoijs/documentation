---
description: Supresses all errors to send a custom one
---

# $suppressErrors

This function suppresses all errors and sends a custom one.

```javascript
$suppressErrors[error message (optional)]
```

```javascript
bot.command({
name: "suppressErrors",
code: `Nothing is wrong with this code!
$suppressErrors[Theres something wrong with this code]`
})
```



From 1.4.0 update, new subfunction, `{error}`has been added. This will return any errors with your custom error message

