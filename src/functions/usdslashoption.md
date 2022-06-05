---
description: An output for slash's option.
---

# $slashOption

`$slashOption`, returns the given argument on slash's option. For choices, it returns the value of choice.

### Usage 

```php
$slashOption[option name]
```

### Fields

| Field | Description | Required |
| :--- | :--- | :--- |
| option name | The name of slash option | yes |

## Example

```javascript
/* Let's say we have a string type slash option like this (message):
/say message: ...
*/
bot.interactionCommand({
  name: "say", 
  prototype: 'slash',
  code: `
  $interactionReply[
    $slashOption[message]
  ]
  `
});
// Returns the text that user has been typed on the slash option.
```
