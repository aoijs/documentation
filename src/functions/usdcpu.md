---
description: Returns the CPU Usage
---

# $cpu

This function returns the cpu usage in percentage

#### Fields

This function has 1 field

1. Type \(Optional\)

Raw Usage: `$cpu[type (optional)]`

#### Options

1. Type - The cpu usage type to count the percentage from

#### Types

1. `os` - System cpu usage
2. `process` - Process cpu usage (default)

#### Usage

```javascript
bot.command({
name: "cpu",
code: `CPU Usage: $cpu`
})
```

![Returns this](<../../.gitbook/assets/image (25).png>)
