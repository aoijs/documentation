---
description: Deletes an interaction message.
---

# $interactionDelete

`$interactionDelete`, as it is name; it deletes the interaction message.

### Usage 

```php
$interactionDelete
```

### Footnote

* This function doesn't work on ephemeral message.

## Example

```javascript
bot.interactionCommand({
  name: "hello",
  prototype: 'slash',
  code: `
  $interactionDelete
  $wait[5s]
  $interactionReply[Hello, world!]
  `
});
```

And it deletes the interaction message 5 seconds later.
