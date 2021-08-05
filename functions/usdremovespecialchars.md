# $removeSpecialChars

This function removes all special characters from the given text.

### Usage

This function has 1 field

1. Text \(Required\)

Raw Usage: `$removeSpecialChars[text]`

#### Options

* Text - The text from which the function would remove the special characters.

For Non-Command Handler:

```javascript
bot.command({
name: "rspecial",
code: `$removeSpecialChars[##&@Beast#@$]`

//Returns: Beast
})
```

For Command Handler

```javascript
module.exports = ({
name: "rspecial",
code: `$removeSpecialChars[##&@Beast#@$]`

//Returns: Beast
})
```
