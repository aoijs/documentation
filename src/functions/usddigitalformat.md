---
Description: Displays the time in digital form.
---
<hr>

# $digitalFormat

This function is which the hours, minutes, and seconds are indicated by digits.

Raw Usage: `$digitalFormat[ms]`
## Field

This function has 1 field
| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| ms | Return milliseconds to digital form. | number | yes |
## Example

```javascript
bot.command({
  name: "digitalFormat",
  code: `
  $digitalFormat[5000000]
  `
//Returns 01:23:20
});
```
