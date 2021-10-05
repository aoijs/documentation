---
description: >-
  Creates a collector of buttons for given message for the provided user in a
  given time
---

# $buttonCollector

## RawUsage

```javascript
$buttonCollector[messageID;userID/everyone;time;customID,customID,...;awaitedcommand,awaitedCommand,...;ErrorContent,ErrorEmbed,ErrorFlag (optional); awaitedcommand for when collector ends (optional)]
```

## Fields

* messageID : ID of the message to create collector for.
* UserFilter : ID of the user for whom the collector should work. "everyone" for every user.
* time : For how long the collector will accept valid interactions
* customIDs... : Row of customIDs the collector will work for.
* awaitedcommand...: Row of awaitedCommands' name , which will get executed according to their position wrt customID when collector recieves a valid interaction
* ErrorMessage : divided into 3 parts \(ErrorContent , ErrorEmbed & ErrorFlag\) the collector will send this error when a user who is not present in UserFilter clicks on the button
* awaitedCommand :an awaitcommand to execute when the Collector ends

## **Example Usage**

```javascript
bot.command({
name:"buttoncollector",
code:`
   $buttonCollector[$get[id];$authorID;1m;click;awaitclick;Only $userName can use this interaction,,64]
   $let[id;$apiMessage[$channelID;hi;;{actionRow:click me,2,1,click};;yes]]
     `
 })
bot.awaitedCommand({
name:"awaitclick",
code:`
   $interactionReply[Hello;;;64]
     `
 })
```

