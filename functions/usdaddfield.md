---
description: addField allows you to add more fields in your embed.
---

# $addField

This function is in charge of adding a new field to the embed, these containing a limit of 1024 characters each and allowing to use 25 fields per embed.

```php
$addField[index;text;value;inline]
```

## Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| index | The embed to add this author to. | integer | yes |
| text | The field text. | string | yes |
| value | The field value. | string | yes |
| inline | The field inline. | boolean | no |

## Examples

Without inline

```javascript
bot.command({
    name: "embed",
    code: `$addField[1;Example Field;Value Field]`
});
```

With inline

```javascript
bot.command({
    name: "embed",
    code: `
    $addField[3;Example Field;Value Field;yes]
    $addField[2;Example Field;Value Field;yes]
    $addField[1;Example Field;Value Field;yes]
    `
});
```





