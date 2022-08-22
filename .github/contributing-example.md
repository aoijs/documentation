---
description: Short description of the function.
---

## $function 

Explanation of the function and how does it work.

> **This function *is not* an official function[^1].**

## Usage
 
> *Declaring with '?' at the ends help to show it as 'optional'*

```php
$function[param1;param2?]
```

## Parameters 

> *If there is even one parameter, it should be used.*

| FIELD | TYPE | DESCRIPTION |
| -------- | -------- | -------- |
| param1 | string | It shows `param1` | 
| param2 | integer | It shows `param2` | 

### Parameter Types
> *Required if the parameter has other options*

* `a` — A type
* `b` — B type

## Example(s)

This returns: ...

```javascript
bot.command({
  name: 'function-name',
  code: `
  $function[index;aoijs]
  `
});
```

[^1]: You can also use footnotes to explain it on your way :)
