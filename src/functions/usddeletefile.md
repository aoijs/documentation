---
description: Used to delete the specified file.
---

# $deleteFile

`$deleteFile` allowing you to delete the specified file.

### Usage

```php
$deleteFile[file]
```

### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| file | The path to the file which is to be deleted | alphanumeric | yes |

## Examples

```javascript
bot.command({
  name: "add",
  code: `
  $deleteFile[./src/data.txt]
  `
}); // Deletes the data.txt file present in src folder
```
