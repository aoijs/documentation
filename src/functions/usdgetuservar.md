---
description: Gets a user's variable value
---

# $getUserVar

This function returns the value of the given variable for the user.

#### Fields

This function has 1 required field

1. Variable \(Required\)
2. User ID \(Optional\)

Raw Usage: `$getUserVar[variable;userID (optional)]`

#### Options

* Variable - The variable value we're getting for the &lt;user&gt;
* User ID - The user's variable value we're getting

#### Usage

Current User's Variable Value

```javascript
bot.command({
name: "get", 
code: `
$getUserVar[variable]`
})
```

Mentioned User's Variable Value

```javascript
bot.command({
name: "get", 
code: `
$getUserVar[variable;$mentioned[1]]`
})
```

