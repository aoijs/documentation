---
description: Merge two or more arrays. 
---

# $arrayConcat

`$arrayConcat` used to merge two or more arrays without does not changing the existing arrays, but instead returning a new array.

### Usage 

```php
$arrayConcat[separator;arrayName...]
```

### Properties

| FIELD | TYPE | DESCRIPTION |
| ----- | ----- | ----- | 
| separator | string | The separator for array elements | 
| arrayName... | string | The arrays going to be merged with separated semicolon |

## Example

```javascript
bot.command({
  name: "array-concat", 
  code: `
  Concatted result:
  $arrayConcat[,;array1;array2]]
  
  $createArray[array2;6;7;8;9;10]
  $createArray[array1;1;2;3;4;5]
  `
  // Creates "newArray" with ten elements that uses "array1" and "array2" is elements.
});
```
