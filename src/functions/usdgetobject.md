---
description: Get object datas.
---

# $getObject

This function returns stringified JSON Object from $createObject/$addObjectProperty.

### Usage

```php
$getObject
```

### Field

| Field | Description | Required |
| :--- | :--- | :--- |
| json | The key & property in the object | no |


#### Example

Without Optional:

```javascript
bot.command({
	name: "getObject",
	code: `
	$getObject
	
	$addObjectProperty[lights;off]
	
	$addObjectProperty[key;on]
	
	$createObject[{}]
	`
/* Returns:
{
	"key": "on",
	"lights":"off"
}
*/
});
```
