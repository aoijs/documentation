---
description: Creates an object that can be used in code.
---

# $createObject

This function creates an object. Simplified terms, its a in-code variable that is only accessible in the current code.

### Usage

```php
$createObject[{json}?]
```

### Field

| Field | Description | Required |
| :--- | :--- | :--- |
| json | The key & property in the object | no |


#### Examples

Without Optional:

```javascript
bot.command({
  name: "createObject",
  code: `
  $getObjectProperty[message]
  
  $addObjectProperty[message;Hello, World!]
  
  $createObject[{}]
  `
//Returns "Hello, World!"

/*For to see how does it get stored.
{ data: { object: { message: 'Hello, World!' } } } */
})
```

With Optional:

```javascript
bot.command({
  name: "createObject",
  code: `
  $getObjectProperty[message]
  
  $createObject[{"message":"Hello Word"}]
  `
//Returns "Hello, World!". We didn't use $addObjectProperty in here.
});
```
