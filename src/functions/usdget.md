---
description : Gets a value of the specified key from $let function.
---

# $get

This function gets a value of the specified key from [$let](./usdlet.md).

## Fields

This function has 1 required field

1. Key \(Required\)

### Usage 
```php
$get[key]
```

## Options

* Key - The key we're getting for the value assigned to it

## Example

```javascript

bot.command({
name: "example',
code: `
$get[ruben]
$let[ruben;gay]
`
})

// $get[ruben] will return 'gay'
```

