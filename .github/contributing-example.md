---
description: Short description of the function.
---

# $function 

Explanation of the function and how does it work.

> **This function *is not* an official function[^1].**

### Usage
 
> *Declaring with '?' at the ends help to show it as 'optional'*

```php
$function[param 1;param 2?]
```

### Fields 

> *Required even for a property*

| Fields | Description | Type | Required |
|--------|-------------|------|----------|
| param 1 | It shows `param 1` | string | yes |
| param 2 | It shows `param 2` | number | no |

#### Param Types 
> *Required if the property has other options*

* `a` — A type
* `b` — B type

## Example(s)

```javascript
bot.command({
  name: 'function-name',
  code: `
  $function[index;aoijs]
  `
// Returns: ...
});
```

[^1]: You can also use footnotes to explain it on your way :)
