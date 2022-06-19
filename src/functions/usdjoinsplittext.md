---
description: Joins the $textSplit indexes by <separator>
---

# $joinSplitText

This function joins the $textSplit values with the new &lt;separator&gt;.

### Usage
```php
$joinSplitText[separator]
```
### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| separator | The separator used to join values |alphanumeric|yes|

## Example
```javascript
bot.command({
name: "join", 
code: `
$joinSplitText[|]
$textSplit[hello-bye-lol;-]`
//Returns: hello|bye|lol
})
```

