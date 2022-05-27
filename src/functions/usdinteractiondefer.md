---
description: Deferring an interaction message.
---

# $interactionDefer

`$interactionDefer`, defers the message for latest 15 minutes which can be used well for `$interactionFollowUp` function. For more detailed information check [$interactionFollowUp](functions/usdinteractionfollowup.md).

### Usage 

```php
$interactionDefer[ephemeral?]
```

### Field

| Field | Description | Required |
| :--- | :--- | :--- |
| ephemeral | Makes the interaction ephemeral | no |

## Example

This will make out interaction message as ephemeral message.

```javascript
bot.interactionCommand({
  name: "hello",
  prototype: 'slash',
  code: `
  $interactionFollowUp[Hello, world!]
  
  $interactionDefer[yes]
  `
});
```
