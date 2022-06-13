---
description: Used for slicing arguments from the given text
---

# $argsSlice

This function slices the given text to return sliced argument.

### Usage 
```php
$textSlice[text;from?;to]
```
### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| text | The text we're slicing | string | yes |
| from | The position from where the slice will start | number (default: 0)| no |
|to|The position where the slice will end|number|yes|


## Examples

- Without optional field

```javascript
bot.command({
name: "slice",
code: `$textSlice[goodbye;3]`
})
```

- With optional field

```javascript
bot.command({
name: "slice",
code: `$textSlice[goodbye;1;3]`
})
```

