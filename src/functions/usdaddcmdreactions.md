---
description: Add reaction to author's message.
---

# $addCmdReactions

`$addCmdReactions` adds single or multiple reactions to author's message.

### Usage

```php
$addCmdReactions[emoji;emoji;...]
```

### Field

| Field | Description | Type |
| :--- | :--- | :--- |
| emoji | A default Discord emoji or a custom emoji with ID | string |

###### Custom Emoji Information

> *Custom Emoji Usage* — `<:emoji:1234567890>` & `<a:emoji:1234567890>` (<\{type\}:\{name\}:\{id\}>) 

* `type` — type of the emoji 
* `name` — name of the emoji
* `id` — id of the emoji

## Examples

With custom emoji:

```javascript
bot.command({
	name: "add-cmd-reaction",
	code: `
	$addCmdReactions[<:mns_neoXD:961249981107413022>;<:mns_lolie:966349758203559977>]
	`
//Adds emojis to author's message.
});
```

With default emoji

```javascript
bot.command({
  name: "add-cmd-reaction",
  code: `
  $addCmdReactions[😋;🤠]
  `
//This also adds emojis to author's message as well.
});
```
