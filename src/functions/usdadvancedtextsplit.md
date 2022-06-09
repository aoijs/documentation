---
description: Text split, but advanced.
---

# $advancedTextSplit

This function basically allows you to have multiple splits in 1 message

### Usage

```php
$advancedTextSplit[text;separator;index;separator2;index2;...]
```

### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| text | The text will get splitted | string | yes |
| seperator | The seperator of the text which is used for the index | string | yes |
| index | The position of the certain text we want to pull from text depending the seperstor | number | yes |

## Example

```javascript
bot.command({
  name: "advanced-text-split",
  code: `
  $advancedTextSplit[hi/bye|ok;/;2;|;1]
  `
});

/* Explanation
Our first seperator is "/" as you see, and the index is "2" so we are splitting it to two and it becomes like this;

hi (bye|ok) 

Now the second seperator is "|" and the index is "1" which will be returned.

(bye) ok
*/
```

And with this function we have claimed `hi/bye|ok`'s **`bye`** argument :)

