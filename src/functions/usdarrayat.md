---
description: Takes an integer value and returns the item at that index.
---

# $arrayAt

`$arrayAt` function used for, the index (position) of the array element to be returned. Returns *nothing* if the given index **can not** be found.

### Usage

```php
$arrayAt[arrayName;index]
```

### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| arrayName | The name of the array | array | yes |
| index | The position of the element | integer | yes |

## Examples

* Let's return **third element**[^1]:

  [^1]: Elements are starting at "apple" element. If we check the third element, we can see "strawberry" stands for it.
  
```javascript
bot.command({
  name: "array-at",
  code: `
  $arrayAt[fruits;3]
  
  $createArray[fruits;apple;banana;strawberry;watermelon]
  `
  // Returns "strawberry"
});
```

* Let's return **last third element**[^2]:

  [^2]: Our 0th element is our last element, which is "watermelon". If we count backwards, we will be seeing -3 is "apple" element.

```javascript
bot.command({
  name: "array-at",
  code: `
  $arrayAt[fruits;-3]
  
  $createArray[fruits;apple;banana;strawberry;watermelon]
  `
  // Returns "apple"
});
```

* Let's return **seventh element**[^3]:

  [^3]: It won't work. Cause, seventh element doesn't exists.

```javascript
bot.command({
  name: "array-at",
  code: `
  $arrayAt[fruits;7]
  
  $createArray[fruits;apple;banana;strawberry;watermelon]
  `
  // No output
});
```
