---
description: Removes useless spaces from given text.
---

# $textTrim

This function removes all useless spaces \(multiple spaces in a row\) from the given text, so all the spaces be replaced with one space.

## Fields
This function has 1 required field

Text (Optional)

### Usage 
```php
$textTrim[text]
```

## Option
- Text - The text whose useless spaces are to be removed.

## Example

```javascript
bot.command({
name: "trim",
code: `
$textTrim[     Hello,         how are      you?]
`
}) // Output: Hello, how are you?
```

