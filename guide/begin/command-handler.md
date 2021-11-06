---
description: Command Handlers can be used for organizing your commands
---

# Command Handler
 **In This Topic We Will Learn About Basic Command Handling**

## Normal Method Vs Command Handling 

**'Normal Methods Are Good'** but if there are too many commands, then the mainFile can get messy and it gets hard to find and update certain commands. Hence to overcome this issue ,**'Command Handlers'** are introduced.

**Command Handlers** not only solve this issue it also makes the mainFile neat and the project more organized.
## How To Make A Command Handler 
```js
'There are 2 methods to make a command Handler:'
'* fs module'//(which won't be discussed here)
'* LoadCommands Class'
```
### Method 
#### Step-1: Setting Up The Handler 

```javascript
 const bot = new aoijs.Bot({
   token: "TOKEN", //Discord Bot Token
   prefix: "PREFIX", //Discord Bot Prefix
   intents: "all" //Discord Intents 
 })

 bot.onMessage() //Allows to execute Commands

 const loader = new aoijs.LoadCommands(bot)
 loader.load(bot.cmd,"./commands/")

 /*
 bot.cmd is object of Collections where the command data will be stored
 "./commands/" is the path of folder where all the commands' code will be present
 */
```
---
#### Step-2 Creating The First File 
* After Setting Up the Handler In Your MainFile. Create A Folder with name **"commands"**
![](../../.gitbook/assets/screenshot-2020-11-23-at-9.54.22-pm.png)

* After Creating The Commands Folder , **create a Folder** (for example : moderation)
![Subfolder could be used as a category like a discord category](../../.gitbook/assets/screenshot-2020-11-23-at-9.57.28-pm.png)

* After That,**Create A JavaScript File** (for example selfKick.js)
![Name of file: commandName.js](../../.gitbook/assets/selfKick.js.png)
---
#### Step-3 : Adding The Code In The File
* Add The Code In Your Newly Created File (here is example of selfkick command)
```javascript
module.exports ={
  name:"selfkick",
  aliases:["sk","bye","exit"],
  code:`
  $kick[$authorId]`
}
```
#### Step-4: Complete
* Now Run Your Project And See The Console Logging All The Commands 
![Console Logging](../../.gitbook/assets/commadLogging.png)
---
## Is This The End?
 * No, [LoadCommands](../../class/loadCommands.md) Class Has Lots Of Features For Which You Can Refer Too [Extra-Features](guide/begin/command-handler-extras.md).