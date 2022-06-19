---
description: Creates variables that can be used later.
---
# $createVar

This function creates variable\(s\) that can be used later.

### Usage 
```php
$createVar[table;varName:varValue...]
```
### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
|table|The name of the table where the variable is to be allocated|alphanumeric|yes|
| var\(s\) | The name of var with value | name:value | yes |

## Example

- Without optional fields

```javascript
bot.command({
name: 'createVar',
code: `$createVar[main;money:0]`
})
```

- With optional fields

```javascript
bot.command({
name: 'createVar',
code: `$createVar[main;money:0;trusted:false]`
})
```

