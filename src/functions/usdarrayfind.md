---
description: Returns the first element provided in array (Depends to query type).
---

# $arrayFind

`$arrayFind` function returns the first element in the provided array that satisfies the provided testing function. 

> If no values satisfy the testing function, **nothing** is returned.

### Usage 

```php
$arrayFind[name;query;queryType?]
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
  name: "array-find", 
  code: `
  $arrayFind[array;10;>]

  $createArray[array;30;10;20;15]
  `
  // Returns "30". Which is first greater than 10 on array elements.
});
```
