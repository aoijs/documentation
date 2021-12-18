---
description: returns the memory usage in MB
---

# $ram

This function returns the memory usage in Megabyte. 

#### Fields

This function has 1 field

1. Type \(Optional\)

Raw Usage: `$ram[type (optional)]`

#### Options

1. Type - The ram usage type

#### Types

* rss - Process memory usage (default)
* heapTotal - Memory allocated to javascript
* heapUsed - Amount of memory used by javascript
* external - Amount of memory used by nodejs (only) including arrayBuffers
* arrayBuffers - Amount of memory used by ArrayBuffer, TypedArray, and Buffer

#### Usage

```javascript
bot.command({
name: "memory", 
code: `
Memory usage: $ram` //Ex: Returns 64.83941650390625
})
```

