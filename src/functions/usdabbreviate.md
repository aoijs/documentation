---
description: Abbreviate numbers.
---

<hr>

# $abbreviate

`$abbreviate` allowing you to abbreviate large numbers.

### Usage
```
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
})
```

With decimal:

```javascript
bot.command({
	name: "abbreviate",
	code: `
	$abbreviate[6900;1]
	`
//Returns: 6.9K
})
```
