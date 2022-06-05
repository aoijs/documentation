---
description: Returns the author's avatar in url format.
---

# $authorAvatar

This function returns picture of who executed the function/command.

### Usage

```php
$authorAvatar[size?;dynamic?;format?]
```

### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| size | Size of the banner | number | no |
| dynamic | Stopping animation (related to animated pictures) | string | no |
| format | Format of the banner (jpg, png etc.) | string | no |

#### Example

Without optional
```javascript
bot.command({
  name: "authorAvatar",
  code: `
  This is my avatar!

  $authorAvatar
  `
//Returns my avatar
});
```

