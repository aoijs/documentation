---
description: Gets message variable value
---

# $getMessageVar

This function returns the value of the specified message ID for the specified variable

## Fields

This function has 1 required field

1. Variable \(Required\)
2. Message ID \(Optional\)

Raw Usage: `$getMessageVar[variable;messageID (optional)]`

## Options

* Variable - The variable value we're getting for the &lt;message&gt;
* Message ID - The message's variable value we're getting

## Usage

Current Message's Variable Value

```javascript
bot.command({
name: "get", 
code: `
$getMessageVar[variable]`
})
```

Specified Message's Variable Value

```javascript
bot.command({
name: "get", 
code: `
$getMessageVar[variable;$message]`
})
```

