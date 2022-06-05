---
description: Adds an attachment to the message.
---

# $attachment

This function allows you to add 'attachments' to a message, like images or videos. If name given, you must specify the extension of the attachment (jpg, png, mp4, etc.)

### Usage

```php
$attachment[url;name.extension]
```

### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| url | The attachment will be sending | url | yes |
| name.extension | The attachment's name along with extension | string | yes |

#### Example

```javascript
bot.command({
  name: "attachment",
  code: `
  $attachment[$authorAvatar;neodevil.png]
  `
//This will return the attachment's name as "neodevil.png"
});
```

