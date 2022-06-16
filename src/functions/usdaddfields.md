---
description: Adds fields to embed message.
---

# $addFields

`$addFields` allows you to add a field to in embed message.

### Usage

```php
$addFields[index:name:text:inline?;...]
```

### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| index | The embed's index | number | yes |
| name | The field's title | string | yes |
| text | The field's description | string | yes |
| inline | For the field be in line or not | boolean | no |

###### Footnotes

> * Field Limit: 25 Fields
> * Field Name Limit: 256 Characters
> * Field Text Limit: 1024 Characters

## Example

```javascript
bot.command({
  name: "add-fields",
  code: `
  $addFields[1;My name:My name is Neo.:yes;My Age:I'm 20 years old.;My Gender:Male.:yes]
  `
});
```

