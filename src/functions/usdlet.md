---
description: Allows you to assign a key to a value.
---
# $let

This function allows you to assign a key to a value. This is identical to [$addObjectProperty](./usdaddobjectproperty.md) but it's easier and doesn't require [$createObject](./usdcreateobject.md).

### Usage 
```php
$let[key;value]
```

### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| key | The name of the key to which the value will be assigned | alphanumeric | yes |
| value | The value to be assigned to the key | alphanumeric | yes |

## Example

```javascript
bot.command({
name: "exmaple",
code: `
$get[ruben]
$let[ruben;gay]
`
})
```

