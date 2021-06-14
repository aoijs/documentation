---
description: Gets a global variable value
---

# $getVar

This function returns the value of the given variable everyone shares

#### Fields

This function has 1 required field

1. Variable \(Required\)

Raw Usage: `$getServerVar[variable]`

#### Options

* Variable - The variable value we're getting for all the users

#### Usage

```javascript
bot.command({
name: "get", 
code: `
$getVar[variable]`
})
```

