---
description: Removes numbers from the provided text.
---

# $removeNumbers
## Usage
```php
$removeNumbers[text]
```
This function has one field.

| Field | Description | Type | Required
| ------------- | ------------- | ------------- | ------------- |
| text | The text to remove numbers from. | string | yes

## Example
```javascript
bot.command({
    name: "example",
    code: `$removeNumbers[123 Hello World! 456]`
})
// Returns "Hello World!"
```
