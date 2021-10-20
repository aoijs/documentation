---
description: Removes special characters from the provided text.
---

# $removeSpecialChars
## Usage
```php
$removeSpecialChars[text]
```
This function has one field.

| Field | Description | Type | Required
| ------------- | ------------- | ------------- | ------------- |
| text | The text to remove special characters from. | string | yes

## Example
```javascript
bot.command({
    name: "example",
    code: `$removeSpecialChars[!%&hi()+=]`
})
// Returns "hi"
```
