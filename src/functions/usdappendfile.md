---
description: Used to add new data to the specified file without replacing the data present in the file.
---

# $appendFile

`$appendFile` allowing you to add new data to the specified file without replacing the data present in the file.

### Usage

```php
$appendFile[file;text;encode?]
```

### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| file | The path to the file in which the data is to be added | alphanumeric | yes |
| text | The text to be added in the file | alphanumeric | yes |
| encode |The encoding style to be implemented on the text being added|alphanumeric|no|

###### Encode Types

* `ascii` — ASCII Code Characterization
* `latin` — Latin Characterization
* `utf8` - Unicode Characterization

## Examples

```javascript
bot.command({
  name: "add",
  code: `
  $appendFile[./src/data.txt;This is a new text;ascii]
  `
// Adds "This is a new text" to the data.txt file present in src folder with ASCII code characterization.
});
```
