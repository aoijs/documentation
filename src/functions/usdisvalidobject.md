---
description: Returns true or false if it's an object
---

# $isValidObject

This function checks if the given string is a valid json object. Returns boolean

```php
$isValidObject[object]
```

### Field

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| object | The string object | string | yes |

###### Footnote

* This function will only work if it's JSON Object 

> `{ "lights":"on" }` is a  JSON Object  
> `{ lights: "off" }` **is not** a JSON Object

#### Example

```javascript
bot.command({
	name: "is-valid-object",
	code:`
	$isValidObject[ { "test": "hi" } ]
	`
})
```