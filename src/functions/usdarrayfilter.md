---
description: Filters the array elements.
---

# $arrayFilter

`$arrayFilter` function filters down to just the elements from the given array that pass the condition.

### Usage 

```php
$arrayFilter[name;query;queryType?;separator?]
```

### Properties

| FIELD | TYPE | DESCRIPTION |
| ----- | ----- | ----- | 
| name | array | The name of the array | 
| query | element | The element we will be queering for every element inside the array |
| queryType? | operator | The comparison operator |
| separator? | symbol | The symbol for seperating filtered elements |

#### Comparison Operators

* `includes` — Including 
* `startsWith` — Starts with
* `endsWith` — Ends with
* `==` — Equal to 
* `!=` — Not equal to
* `>` — Greater than
* `<` — Less than
* `>=` — Greater than or equal to
* `<=` — Less than or equal to

## Example

```javascript
bot.command({
  name: "array-filter", 
  code: `
  $arrayFilter[array;10;>;, ]

  $createArray[array;30;10;20;15]
  `
  // Returns "30, 20, 15". Which is greater than 10.
});
```
