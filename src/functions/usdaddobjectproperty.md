---
description: Adds a property name to an existing object.
---

# $addObjectProperty

With this function you can add properties \(Keys\) to an object previously created in JSON format.

### Usage

```php
$addObjectProperty[key;value]
```

### Fields

| Field | Description | Required |
| :--- | :--- | :--- |
| key | The name of the property | yes |
| value | The value that's assigned to the key | yes |

## Example

```javascript
bot.command({
  name: "add-object-property",
  code: `
  $getObjectProperty[lights]
  
  $addObjectProperty[lights;off]
  
  $createObject[{}]
  `
});
```
