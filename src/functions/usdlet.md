---
description : Allows you to assign a key to the variable.
---

# $let

This function allows you to assign a key to a value. This is identical to [$addObjectProperty](usdaddobjectproperty.md) but it's easier and doesn't require [$createObject](usdcreateobject.md).

## Fields

This function has 2 fields.

1. Key \(Required\)
2. Value \(Required\)

### Usage: 
```php
$let[key;value]
```

## Options

* Key - The key that will be called with [$get](usdget.md)
* Value - The value assigned to the &lt;key&gt;

## Example

```javascript
bot.command({
name: "exmaple",
code: `
$get[ruben]
$let[ruben;gay]
`
}) 
// Output: gay
```

