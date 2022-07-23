---
description: Changes the bot's username.
---

# $setBotUsername

This function set's the bot's username to given text.

## Usage

```php
$setBotUsername[newName]
```

### Property

| FIELD | TYPE | DESCRIPTION |
| ----- | ----- | ----- | 
| newName | string | The text will be bot's username | 

## Example

```javascript
bot.command({
  name: "set-bot-username",
  code: `
  Successfully updated my name to $username devil!
  
  $setBotUsername[$username devil]
  `
});
```
