---
description: Deletes the original interaction Response.
---

# $interactionDelete

### Description

```javascript
"Deletes the original interaction Response."
```

### Usage

```javascript
"$interactionDelete"
```

> **Note**: This doesn't supports ephemeral messages.

### Example

```javascript
bot.interactionCommand({
name:"ping",
code:`
$interactionDelete
$wait[5s]
$interactionReply[pong!;;;0;4]
`
})
