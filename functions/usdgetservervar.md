---
description: Gets server variable value
---

# $getServerVar

This function gets the given variables value for the current or specified server

#### Fields

This function has 1 required field

1. Variable \(Required\)
2. Server ID \(Optional\)

Raw Usage: `$getServerVar[variable;serverID (optional)]`

#### Options

* Variable - The variable value we're getting for the &lt;server&gt;
* Server ID - The server's variable value we're getting

#### Usage

Current Server's Variable Value

```javascript
bot.command({
name: "get", 
code: `
$getServerVar[variable]`
})
```

Specified Server's Variable Value

```javascript
bot.command({
name: "get", 
code: `
$getServerVar[variable;$message]`
})
```

