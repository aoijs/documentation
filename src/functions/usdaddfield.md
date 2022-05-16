---
description: Adds field to embed message.
---

# $addField

`$addField` allows you to add a field to in embed message.

### Usage

```php
$addField[index;name;text;inline?]
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

## Examples

Without in line:

```javascript
bot.command({
  name: "add-field",
  code: `
  $addField[1;Your Username;Hello, I am Neo!]
  `
});
```

With in line:

```javascript
bot.command({
  name: "add-field",
  code: `
  $addField[1;My Gender;Male.;yes]
  
  $addField[1;My Age;I'm 20 years old.;yes]
  
  $addField[1;My name;My name is Neo.;yes]
  `
});
```
