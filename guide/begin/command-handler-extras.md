# Extra Features
**As we have a basic command Handler , Let's talks about some features.**
## Features 
### Callback Commands Handlers 
* LoadCommands has a reserved property named **"type"** which determines the type of the command .
* By default , it's set to **"default"** which is our bot.command.so if we set the value of type, we can also set the type of command we want it to be load as.

#### Example
* For Example,we are making a command for **"bot.onMessageDelete()"** Callback.
* after adding **"bot.onMessageDelete()"** in your mainFile , add this code by creating a new file inside moderation folder.
 ```javascript
 module.exports = {
    channel:"$channelId",
    name:"deleteLog", // name property is not necessary it's just for logging the command (if this is not present channel property will be used for logging)
    type:"messageDelete",
    code:`
      A message was deleted!!
      Message:"$message"`
    }
```
#### logged 
* now run the project.Check! the command has been logged as messageDelete , which means that your command will be executed , when someone deletes the message

#### Types 
* You can check all the available types in [here](../../options/commandTypes.md)

### Update commands 
*Using LoadCommands class also enables a special function: **"$updateCommands"**.

This function updates all the new changes to the commands without restarting!

### Multiple Commands On Same File
* LoadCommands.load() Accept arrays in module.exports,which means, You can also add multiple Commands in Same File!

#### Example
* Right now we have 2 files **"deletelog.js"** and **"selfkick.js"**

 Lets Combine Them!
```javascript
 module.exports = [{
    channel:"$channelId",
    name:"deleteLog", // name property is not necessary it's just for logging the command (if this is not present channel property will be used for logging)
    type:"messageDelete",
    code:`
      A message was deleted!!
      Message:"$message"
`
    },{
  name:"selfkick",
  aliases:["sk","bye","exit"],
  code:`
  $kick[$authorId]
`
}]
```
#### logged 
* now run the project.Check! both commands are logged now.
 ![](../../.gitbook/assets/Screenshot_2021-08-06-16-09-09-49.png)

-----