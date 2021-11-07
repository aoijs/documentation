# Slash Commands

## Introduction

Slash Commands are the new, exciting way to build and interact with apps on Discord. With Slash Commands, all you have to do is type `/` and you're ready to use your favorite bot. Users can learn everything your bot does and easily find new features as you add them. Validation, error states, and helpful UI walks them through your commands, meaning they can get it right the first time, especially on mobile. You now have one more ally in the fight against your phone's autocorrect. Slash Commands set your users up for success instead of confusion and frustration. They separate how users think and how your code works, meaning no matter how complex your codebase and commands may get, people who love your bot will find it approachable and easy to use.

![Here is an example of what they&apos;d look like](../../.gitbook/assets/image%20%2850%29.png)

## Getting Started

When getting started with slash commands, it's important to know what you should have.

### Correct OAuth2 Link

Your bot invitation link must have this checked.

![](../../.gitbook/assets/image%20%284%29.png)

{% hint style="warning" %}
**Re-invite** your bot or else it will not work
{% endhint %}

### Knowing the limits

Each guild can have 50 slash commands. Remember, everything can be abused, as well as slash commands so use at own risk

### Important Information

2 Slash Commands can not be the same name in the same guild

Slash command names can not contain special symbols and must be shorter than 32 characters

Slash Command Information break down

![BLUE: NAME/TRIGGER \| RED/ORANGE: DESCRIPTION](../../.gitbook/assets/image%20%2873%29.png)

## The Functions

Let's first get to know the functions and how to use them

### $createSlashCommand

This function will create a slash command!

```text
$createSlashCommand[guildID;name;description;options (optional)]
```

```javascript
bot.command({
name: "create",
code: `$createSlashCommand[$guildID;AOIjs;A cool slash command for AOIjs]`
/*
    Code Breakdown:
This will make a slashcommand named "AOIjs" (meaning you'd do /AOIjs),
the description will say "A cool slash command for AOIjs"
*/
})
```

Using function will `options` filled out

```javascript
bot.command({
name: "create",
code: `$createSlashCommand[$guildID;AOIjs;A cool slash command for AOIjs;message]`
/*
    Code Breakdown:
    Same thing as above but adds a required field. Example in imagine below
*/
})
```

![Example](../../.gitbook/assets/image%20%2834%29%20%282%29.png)

### $getSlashCommandID

This function gets the specified slash command's id that we can use later

```javascript
$getSlashCommandID[name;guildID]
```

```javascript
bot.command({
name: "getID",
code: `$getSlashCommandID[AOIjs]`
/*
    Code Breakdown:
This will get the ID of the slashcommand we created
*/
})
```

### $getSlashCommandOptions

This function gets the &lt;options&gt; in a slash command \(if provided\)

```javascript
$getSlashCommandOptions[name;guildID (optional)]
```

```javascript
bot.command({
name: "getOptions",
code: `$getSlashCommandOptions[AOIjs]`
/*
    Code Breakdown:
This will get the availible options for slash commands
*/
})
```

### $modifySlashCommand

This function will modify an existing slash command

```javascript
$modifySlashCommand[guildID;commandID;name;description;options (optional)]
```

```javascript
bot.command({
name: "modify",
code: `$modifySlashCommand[$getSlashCommandID[AOIjs];AOIjs;A modified description... wow]`
/*
    Code Breakdown:
This will modify the slash command description. We get
the ID from using '$getSlashCommandID'
*/
})
```

### $deleteSlashCommand

This function deletes the specified slash command

```text
$deleteSlashCommand[guildID;name/id]
```

```javascript
bot.command({
name: "delete",
code: `$deleteSlashCommand[$guildID;AOIjs]`
/*
    Code Breakdown:
This will delete our created slashcommand that we made.
*/
})
```

{% hint style="danger" %}
Function/Callback below are **needed** for slash commands to work
{% endhint %}

### bot.onInteractionCreate\(\)

This will execute if a slash command is used

```javascript
bot.interactionCommand({ //command
name: "slash command name", //name of the slash command
code: `code` // code that will be executed if slash command triggered
})
bot.onInteractionCreate() //callback itself
```

```javascript
bot.interactionCommand({
name: "AOIjs", 
code: `AOIjs is an awesome package!`
/*
The code will be execute once /AOIjs has been ran
*/
})
bot.onInteractionCreate()
```

### $interactionReply

This function sends a message to the channel when the slash command in executed

```javascript
$interactionReply[message]
```

```javascript
bot.interactionCommand({
name: "AOIjs", 
code: `
$interactionReply[AOIjs is an awesome package!]
` 
})
bot.onInteractionCreate()
```

## Creating a simple slash command

### Making the slash

Let's make a simple slash command that will reply with the current package version!

```javascript
bot.command({
name: "slash",
code: `
$createSlashCommand[$guildID;version;Return's Aoi.js's current version]`
//This will make our slash command
})
```

### Callback

```javascript
bot.interactionCommand({
 name: "version", 
 code: `$interactionReply[Package Version: $packageVersion]`
 })
 bot.onInteractionCreate()
```

