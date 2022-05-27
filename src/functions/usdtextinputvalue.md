---
description: An output for interaction modal's option.
---

# $textInputValue

`$textInputValue`, returns the answer typed on modal.

### Usage 

```php
$textInputValue[customID]
```

### Fields

| Field | Description | Required |
| :--- | :--- | :--- |
| customID | Custom ID of text input | yes |

## Example

```javascript
//Let's say user typed "4" on input
bot.interactionCommand({
  name: "profile", 
  prototype: 'slash',
  code: `
  $interactionModal[Answer the question;questionModal;
    {actionRow:
      {textInput:2+2=?:1:answerInput}
    }
  ]
  `
});

bot.interactionCommand({
  name: "questionModal",
  prototype: 'modal',
  code: `
  $interactionReply[$textInputValue[answerInput]]
  `
});
//Returns: 4
```
