---
description: Removes new lines from the provided text.
---

# $removeNewLines
## Usage
```php
$removeNewLines[text]
```
This function has one field.

| Field  | Description | Type | Required
| ------------- | ------------- | ------------- | ------------- |
| text  | The text to remove new lines from.  | string | no

## Example
```javascript
bot.command({
    name: "example",
    code: `$removeNewLines[hi
    hello
    hey]`
})
// Returns "hi hello hey"
```
