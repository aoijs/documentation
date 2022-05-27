---
description: updates an deferred interaction message.
---

# $interactionDeferUpdate

`$interactionDeferUpdate`, defers the interaction message will be updated. 

### Usage 

```php
$interactionDeferUpdate[ephemeral?]
```

### Field

| Field | Description | Required |
| :--- | :--- | :--- |
| ephemeral | Makes the interaction ephemeral | no |

## Example

This will make out interaction message as ephemeral message, while updating the old message.

```javascript
bot.interactionCommand({
  name: "hello",
  prototype: 'slash',
  code: `
  $interactionReply[
    Hello, world!
    ;
    ;{actionRow:{button:Hello bot!:1:helloBtnID:false:👋}}
  ]
  `
});

bot.interactionCommand({
  name: "helloBtnID", //Button Custom ID
  prototype: 'button', //Defining the interaction is the button
  code: `
  $interactionEdit[
    ;{newEmbed:
      {description:The message is now an embed!}
    }
  ]
  
  $interactionDeferUpdate
  `
});
```
