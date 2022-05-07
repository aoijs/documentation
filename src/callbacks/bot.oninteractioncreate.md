---
description: Used to execute a slash command or button or menu
---

# bot.onInteractionCreate()
This callback is used to execute a slash command, button or menu when they are called.

## Prototypes
- slash - for slash command
- button - for button component
- selectMenu - for select menu component

{% hint style="warning" %} Keep in mind that wherever you use the callback, you need to use bot.onInteractionCreate() in the main file to execute the callback! {% endhint %}

## Usage

- Normal Usage

```js
bot.interactionCommand({
 name: "name of the component", 
 prototype : 'slash/button/selectMenu',
 code: `$interactionReply[...code...]`
 })
 bot.onInteractionCreate() // callback itself
```

- Usage in bot command

```js
bot.command({
 name: "name of the component", 
 type: "interaction",
 prototype : "slash/button/selectMenu",
 code: `$interactionReply[...code...]`
 })
```

- Usage in example code

```js
bot.interactionCommand({
 name: "aoijs", // A slash command with the name aoijs must be created to execute this callback
 prototype : 'slash',
 code: `$interactionReply[Hello I am slash command!]`
 })
 bot.onInteractionCreate() // callback itself
```


## Advanced Interaction Command
- If you want to make a more advanced interaction command *i.e. retrieve user inputs or something else*, then take a look at this [guide](https://github.com/DevMike123/documentation/blob/v5.1.2/src/guide/advanced-guides/slash-commands.md).

