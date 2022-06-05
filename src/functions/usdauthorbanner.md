---
description: Show author's banner.
---

# $authorBanner

This function will show author's banner, if there's not a banner; it will return **`null`**.

### Usage 

```php
$authorBanner[size?;dynamic?;format?]
```

### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| size | Size of the banner | number | no |
| dynamic | Stopping animation (related to animated pictures) | string | no |
| format | Format of the banner (jpg, png etc.) | string | no |

## Example

```javascript
bot.command({
  name: "author-banner",
  code: `
  Here's your banner!
  
  $authorBanner
  `
});
```
