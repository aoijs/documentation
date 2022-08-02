---
description: Command Handlers can be used for organizing your commands
---

## Normal Method Vs Command Handling

**Normal methods are good** but if there are too many commands, then the main file can get messy and it gets hard to find and update certain commands. 

Hence to overcome this issue, **Command Handler** are introduced.

**Command Handlers** not only solve this issue it also makes the main file neat and the project more organized.

## How to make a command handler

### Step-1: Setting Up The Handler

```javascript
const aoijs = require("aoi.js")

const bot = new aoijs.AoiClient({
  token: "DISCORD BOT TOKEN",
  prefix: "DISCORD BOT PREFIX",
  intents: ["GUILDS", "GUILD_MESSAGES"]
})

bot.onMessage() //Allows to execute Commands

const loader = new aoijs.LoadCommands(bot)
loader.load(bot.cmd,"./commands/")

 /*
 bot.cmd is object of Collections where the command data will be stored
 "./commands/" is the path of folder where all the commands' code will be present
 */
```

***

### Step-2: Creating the file

* After Setting up the handler in your main file, create a folder with the name **`commands`** ![](../discord-examples/assets/screenshot-2020-11-23-at-9.54.22-pm.png)
* After creating the commands folder, **create a new sub folder** (for example: **`moderation`**) ![Subfolder could be used as a category like a discord category](../discord-examples/assets/screenshot-2020-11-23-at-9.57.28-pm.png)
* After, **Create a JavaScript file** (for example selfKick.js)

### Step-3: Adding the code onto the file

* Add the following code onto your new file (`selfkick.js` in this example)

```javascript
module.exports ={
  name:"selfkick",
  aliases:["kickmyself"],
  code:`
  $kick[$authorID]`
}
```

## Multiple Commands On Same File

* LoadCommands.load() accepts arrays in module.exports, which allows to add multiple Commands in same file.

* LoadCommands has a reserved property named **"type"** which determines the type of the command. (not needed always)

### Example

* Right now we have two files **`deletelog.js`** and **`selfkick.js`**

> deletelog.js is a new command file, it can be anything you want

Lets Combine Them!

```javascript
 module.exports = [{
    channel: "$channeLID",
    name: "deleteLog", // name property is not necessary it's just for logging the command (if this is not present channel property will be used for logging)
    type: "messageDelete",
    code:`
    A message was deleted!!
    Message: "$message"`
    },
    {
  name: "selfkick",
  aliases:["kickmyself"],
  code:`
  $kick[$authorID]`
}]
```

### Update commands

Using LoadCommands class also enables a special function: **`$updateCommands`**.

This function updates all the new changes to the commands without restarting the Client.