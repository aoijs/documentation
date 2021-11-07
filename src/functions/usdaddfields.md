---
description: addFields allows you to adds more fields to your embed.
---

# $addFields

This function is in charge of adding new fields to the embed, these containing a limit of 1000 characters each and allowing to use 10 fields in one function.

```php
$addFields[index;text;value;inline]
```

## Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| index | The embed to add this author to. | integer | yes |
| text | The field text. | string | yes |
| value | The field value. | string | yes |
| inline | The field inline. | boolean | no |

#### Usage

Without inline

```javascript
bot.command({
    name: "fields",
    code: `$addFields[1;This is name part:and this is content;...]`
});
```

With inline

```javascript
bot.command({
    name: "fields",
    code: `
    $addFields[1;Inline #:1:yes;1:Inline #:2:yes;...]
    `
});
```




