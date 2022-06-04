---
description: Add reactions to bot's message.
---

# $addReactions

`$addReactions` allows to add reactions to bot's response.

### Usage

```php
$addReactions[emoji;...]
```

### Fields

| Field | Description | Type |
| :--- | :--- | :--- | 
| emoji | The emoji going to be reacted on bot's response | string | 


## Example

```javascript
bot.command({
  name: "react",
  code: `
  $addReactions[🌸;🌺]
  
  Hi, take a flower.
  `
//Added these flowers on bot's "Hi, take a flower." message.
});
```
