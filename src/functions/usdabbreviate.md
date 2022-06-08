---
description: Abbreviate numbers.
---

# $abbreviate

This function allows you to abbreviate large numbers.

### Usage

```php
$abbreviate[number;decimal?]
```

### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| number | The number is going to abbreviated | number | yes |
| decimal | Separates the number in a decimal way | number | no |

###### Abbreviation Types

* `k` — thousands
* `m` — millions
* `b` — billions
* `t` — trillions

## Examples

Without decimal:

```javascript
bot.command({
  name: "abbreviate",
  code: `
  $abbreviate[6900]
  `
//Returns: 7K
});
```

With decimal:

```javascript
bot.command({
  name: "abbreviate",
  code: `
  $abbreviate[6983;1]
  `
//Returns: 6.9K
});
```
