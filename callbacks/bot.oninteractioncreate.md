---
description: >-
  An event that gets executed, if the bot sees a user clicks a button on a
  server. To let the bot listen to the event, add one bot.onInteractionCreate()
  callback inside your mainfile.
---

# bot.onInteractionCreate

### Buttons

#### Usage

```javascript
bot.interactionCommand({
name: "Interaction name",
prototype: "button",
code: `Code here`
})
```

#### Example Command:

```javascript
bot.interactionCommand({
name: "hi",
prototype: "button",
code: `Whats up $username`
})
```

### Slash commands

#### Usage

```javascript
bot.interactionCommand({
name: "Interaction name",
code: `Code here`
})
```

### Example Command:

```javascript
bot.interactionCommand({
name: "hi",
code: `Whats up $username`
})
```

### Componets

`$interactionReply[Plain message;embeds (leave blank if none);componets (optional);flags (optional);type (optional)]` 

 Use this to send a message when the interaction gets triggered

`$interactionEdit[Plain message;embeds (leave blank if none);componets (leave bank if none)]` 

 Edits the Interaction Message from $interactionReply

#### Example

```javascript
bot.interactionCommand({
name: "example",
prototype: "button",
code: `
$interactionEdit[Hi!;{title:Edited}{description:This message was edited}]
$wait[3s]
$interactionReply[Hello!;{title:Hello $username}{description:nom}]
`
```

