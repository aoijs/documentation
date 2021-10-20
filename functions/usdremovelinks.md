---
description: Removes links from the provided text.
---

# $removeLinks
## Usage
```php
$removeLinks[text]
```
This function has one field.

| Field | Description | Type | Required
| ------------- | ------------- | ------------- | ------------- |
| text | The text to remove links from. | string | yes

## Example
```javascript
bot.command({
    name: "example",
    code: `$removeLinks[Aoi.JS: https://aoi.js.org/]`
})
// Returns "Aoi.JS:"
```
