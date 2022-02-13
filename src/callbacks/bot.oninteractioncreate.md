---
description: It is used to execute a block of code when an interaction such as button/interaction is used. To use the callback, add bot.oninteractioncreate() in your main file.
---

# bot.onInteractionCreate
This callback is used to execute a block of code when an interaction such as button/interaction is used.

## Prototypes
1. slash (Used for slash commands)
2. button (Used for buttons)

## Usage
- With slash command

```js
bot.interactionCommand({
name: "aoijs", 
prototype : 'slash',
code: `$interactionReply[AOIjs is an awesome package!]`
/*
The code will be execute once /aoijs has been ran
*/
})
bot.onInteractionCreate()
```

- With button

```js
bot.interactionCommand({
name: "aoijs", 
prototype : 'button',
code: `$interactionReply[AOIjs is an awesome package!]`
/*
The code will be execute once /aoijs has been ran
*/
})
bot.onInteractionCreate()
```

