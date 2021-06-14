---
description: Get The Global User Var
---

# $getGlobalUserVar

This function returns the value of the given value for the given user.

#### Fields

This function has 1 required field

1. Variable \(Required\)
2. User ID \(Optional\)

Raw Usage: `$getGlobalUserVar[variable;userID (optional)]`

#### Options

* Variable - The variable value we're getting for the &lt;user&gt;
* User ID - The user's variable value we're getting

#### Usage

Current User's Variable Value

```javascript
bot.command({
name: "get", 
code: `
$getGlobalUserVar[variable]`
})
```

Mentioned User's Variable Value

```javascript
bot.command({
name: "get", 
code: `
$getGlobalUserVar[variable;$mentioned[1]]`
})
```





