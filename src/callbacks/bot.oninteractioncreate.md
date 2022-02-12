---
description: It is used to execute a block of code when an interaction such as button/interaction is used. To use the callback, add bot.oninteractioncreate() in your main file.
---

# bot.onInteractionCreate
This callback is used to execute a block of code when an interaction such as button/interaction is used.

#### Raw Usage
```php
$interactionReply[content;embeds?;components?;files?;ephemeral?]
```

## Options
1. content (required)
2. embeds (optional)
3. components (optional)
4. files (optional)
5. ephemeral (optional)

## Prototypes
1. slash (Used for slash commands)
2. button (Used for buttons)

## Usage
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

