# Slash Commands

## Introduction

Slash Commands are the new, exciting way to build and interact with apps on Discord. With Slash Commands, all you have to do is type `/` and you're ready to use your favorite bot. Users can learn everything your bot does and easily find new features as you add them. Validation, error states, and helpful UI walks them through your commands, meaning they can get it right the first time, especially on mobile. You now have one more ally in the fight against your phone's autocorrect. Slash Commands set your users up for success instead of confusion and frustration. They separate how users think and how your code works, meaning no matter how complex your codebase and commands may get, people who love your bot will find it approachable and easy to use.

![Here is an example of what they'd look like](<../../../../.gitbook/assets/image (50).png>)

## Getting Started

When getting started with slash commands, it's important to know what you should have.

### Correct OAuth2 Link

Your bot invitation link must have this checked.

![](<../../../../.gitbook/assets/image (4).png>)

{% hint style="warning" %}
**Re-invite** your bot or else it will not work
{% endhint %}

### Knowing the limits

Each guild can have 50 slash commands. Remember, everything can be abused, as well as slash commands so use at own risk

### Important Information

2 Slash Commands can not be the same name in the same guild

Slash command names can not contain special symbols and must be shorter than 32 characters

Slash Command Information break down

![BLUE: NAME/TRIGGER | RED/ORANGE: DESCRIPTION](<../../../../.gitbook/assets/image (73).png>)

## The Functions

Let's first get to know the functions and how to use them

### $createApplicationCommand

This function will create a slash command!

```
$createApplicationCommand[guildID/global;name;description;defaultPermission(true/false);type(slash/user/message) (optional);options (optional)]
```

```javascript
bot.command({
name: "create",
code: `$createApplicationCommand[$guildID;aoijs;a cool slash command for aoi.js;true]`
/*
    Code Breakdown:
This will make a slashcommand named "aoijs" (meaning you'd do /aoijs),
the description will say "a cool slash command for aoijs"
*/
})
```

Using function will `options` filled out

```javascript
bot.command({
name: "create",
code: `$createApplicationCommand[$guildID;aoijs;a cool slash command for aoijs;true;slash;message:sends a message:true:3]`
//or
      `$createApplicationCommand[$guildID;aoijs;a cool slash command for aoijs;true;slash;{string:message:sends a message:yes}]`
//or
      `$createApplicationCommand[$guildID;aoijs;a cool slash command for aoijs;true;slash;{
               "name" : "message",
               "description" : "sends a message",
               "type" : 3,
               "required" : true
      }]`
})

/*
    Code Breakdown:
    Same thing as above but adds a required field. Example in imagine below
*/
```

![Example](<../../../../.gitbook/assets/image (34) (2).png>)

### $getApplicationCommandID

This function gets the specified application command's id that we can use later

```javascript
$getApplicationCommandID[name;guildID/global (optional : global as default)]
```

```javascript
bot.command({
name: "getID",
code: `$getApplicationCommandID[aoijs;$guildId]`
})

/*
    Code Breakdown:
This will get the ID of the slashcommand we created
*/
```

**NOTE**

> if $getApplicationCommandID doesnt return ID and SLash Command Exists, Then eval `$fetch[command]` for global commands and `$fetch[guildCommand;guildid]` for guild commands to fetch all commands and then try again

### $getApplicationCommandOptions

This function gets the \<options> in a slash command (if provided)

```javascript
$getApplicationCommandOptions[name;guildID/global (optional : global as default)]
```

```javascript
bot.command({
name: "getOptions",
code: `$getApplicationCommandOptions[aoijs;$guildId]`
/*
    Code Breakdown:
This will get the availible options for slash commands
*/
})
```

### $modifyApplicationCommand

This function will modify an existing slash command

```javascript
$modifyApplicationCommand[guildID/global;commandID;name;description;type(optional);options (optional);defaultPermission(optional)]
```

```javascript
bot.command({
name: "modify",
code: `$modifyApplicationCommand[$guildId;$getApplicationCommandID[aoijs];aoijs;a modified description... wow]`
/*
    Code Breakdown:
This will modify the slash command description. We get
the ID from using '$getApplicationCommandID'
*/
})
```

### $deleteApplicationCommand

This function deletes the specified slash command

```
$deleteSlashCommand[guildID/global;id]
```

```javascript
bot.command({
name: "delete",
code: `$deleteSlashCommand[$guildID;$getApplicationCommandId[aoijs]]`
/*
    Code Breakdown:
This will delete our created slashcommand that we made.
*/
})
```

{% hint style="danger" %}
Function/Callback below are **needed** for slash commands to work
{% endhint %}

### bot.onInteractionCreate()

This will execute if a slash command is used

```javascript
bot.interactionCommand({ //command
name: "slash command name", //name of the slash command
prototype : 'slash',
code: `code` // code that will be executed if slash command triggered
})
bot.onInteractionCreate() //callback itself
```

```javascript
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

### $interactionReply

This function sends a message to the channel when the slash command in executed

```javascript
$interactionReply[message;embeds?;components?;files?;ephemeral(yes/no)]  //? means optional
```

```javascript
bot.interactionCommand({
name: "aoijs",
prototype : 'slash',
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
$createApplicationCommand[$guildID;version;return's aoi.js's current version;true]`
//This will make our slash command
})
```

### Callback

```javascript
bot.interactionCommand({
 name: "version", 
 prototype : 'slash',
 code: `$interactionReply[Package Version: $packageVersion]`
 })
 bot.onInteractionCreate()
```

## Creating Advanced Slash Commands

### Making the slash

```javascript
bot.command({
name: "slash",
code: `
$createApplicationCommand[$guildID;send-dm;make the bot send a dm to a user;true;slash;user:user to dm:true:6;message:message to send to user:true:3]
`
})
```

### Callback

```javascript
bot.interactionCommand({
 name: "send-dm", 
 prototype : 'slash',
 code: `
 $sendDM[{newEmbed:{title:You Recieved a DM!}{description:Someone sent you a dm!}{field:Author:<@$interactionData[author.id]> | $userTag[$interactionData[author.id]]}{field:Message:$interactionData[options.data[1].value]}};$interactionData[options.data[0].value]]
 $interactionReply[Successfully sent dm to **$userTag[$interactionData[options.data[0].value]]**. Message: **$interactionData[options.data[1].value]**;;;;yes]
 `
 })
  bot.onInteractionCreate()
```

`$interactionData[options.data[0].value]`=> Option 1

`$interactionData[options.data[1].value]`=> Option 2

And so on...
