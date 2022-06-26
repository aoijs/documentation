---
description: Returns URL for given user's avatar.
---

# $userAvatar

This function returns the URL for the given user's avatar.

### Usage

```php
$userAvatar[userID;size?;dynamic?;format?]
```

### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| userID | The ID of the user | number | yes |
| size | Size of the banner | number | no |
| dynamic | Stopping animation (related to animated pictures) | string | no |
| format | Format of the banner (jpg, png etc.) | string | no |


## Example 

```javascript
bot.command({
  name: "user-avatar",
  code: `
  $userAvatar[285118390031351809;1024;no;jpg]
  `
});
```
