---
description: Checks if the specified file exists.
---

# $fileExists

`$fileExists` allowing you to check if the specified file exists.

### Usage

```php
$fileExists[file]
```

### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| file | The path to the file which is to be checked | alphanumeric | yes |

## Examples

```javascript
bot.command({
  name: "check",
  code: `
  $fileExists[./src/data.txt]
  `
}); // Checks if the data.txt file present in src folder exists.
```
