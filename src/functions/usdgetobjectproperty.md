---
description: Gets an key's value from object.
---

# $getObjectProperty

This function gets the property value from specified key.

### Usage

```php
$getObjectProperty[key]
```

### Field

| Field | Description | 
| :--- | :--- | 
| key | The key's name that wants to receive value of key | 

#### Example

```javascript
bot.command({
	name: "getObjectProperty",
	code: `
	$getObjectProperty[mods]
	
	$addObjectProperty[mods;on]
	
	$createObject[{}]
	`
// Returns: on
});
```
