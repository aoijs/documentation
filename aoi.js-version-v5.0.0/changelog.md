# Changelog
--------------------------------------
## Bot 
>**Bot class initialisation has been changed severely.**
>
>**Some properties have either renamed or removed and some new properties are added.**
>
>***SUMMARY*** 

>**@properties**

>```diff
>+intents
>+debugs
>+events
>+cache
>+respondOnEdit
>+database

>```diff
>-supressAll :boolean
>+suppressAllErrors :boolean
>
>-fetchInvites: boolean
>+fetchInvites:{enabled:boolean, cacheInviters: boolean}
>
>-errorMessage:string
>+errorMessage:["content","embeds", "components","files"]

>```diff
>-db
>-databasePath 
>-boosterToken 
>-disableFunctionsStarting

> [You Can Check Those Properties In Details Here](../options/botOptions.md)

>**@commands**

>```diff
>-bot.loadCommands
>-bot.musicStartCommand
>-bot.musicEndCommand 

>```diff
>+bot.stickerCreateCommand
>+bot.stickerUpdateCommand 
>+bot.stickerDeleteCommand 
>+bot.stageInstanceCreateCommand
>+bot.stageInstanceUpdateCommand
>+bot.stageInstanceDeleteCommand 
>+bot.threadCreateCommand
>+bot.threadUpdateCommand
>+bot.threadDeleteCommand
>+bot.threadListSyncCommand
>+bot.threadMemberUpdateCommand
>+bot.threadMembersUpdateCommand
>+bot.guildUnavailableCommand
>+bot.memberAvailableCommand
>+bot.membersChunkCommand
>+bot.reactionRemoveAllCommand
>+bot.reactionRemoveEmojiCommand

>**@events**

>```diff
>-bot.onFunctionError 

>```diff
>+bot.onStickerCreate/Update/Delete 
>+bot.onThreadCreate/Update/Delete/ListSync/MemberUpdate/MembersUpdate 
>+bot.onMemberAvailable
>+bot.onMembersChunk 
>+bot.onReactionRemoveAll/Emoji 
>+bot.onStageInstanceCreate/Update/Delete 
>+bot.onGuildUnavailable 
## Voice 
>**Music system has been Seperated From Bot Class into a seperate Voice Class with its own events**
>
>**Thus,it has its own events and cmds** 

>**@usage**
>```ts
>new Aoijs.Voice(bot:Bot,ytdlOptions:Ytdl,scdlOption:Scdl,cacheOption:Cache)

>[For Detail Usage,You Can check here](../class/voice.md)

>**@commands**

>```diff
>+musicStartCommand
>+musicEndCommand
>+MusicErrorCommand 

>**@events**

>```diff
>+onMusicStart/End/Error

## Lavalink
>**Lavalink has been Seperated into. a new class**

>**@usage**

>```ts 
>const lava = new Aoijs.lavalink(bot:Bot) ;
>lava.createLavalinkConnection(url: string,password:string,debug:boolean) 

>**@events**

>```diff
>+onMusicStart/End/Error

## LoadCommands
>**class to load Commands and Files**

>**@usage** 

>```ts
>const loader = new Aoijs.LoadCommands(bot:Bot)
>loader.load(bot.cmd:Record<string:Group>,path:string) 

>**@methods**

>```ts
>+ load(cmds:Record<name,Group>,path: string,debug?:boolean)
>+ setColor(options:Record<string,Array<string>>)
>+ update(debug?: boolean)

>**[Check Here For More Info](../class/loadCommands.md)**

## ClientShard 
>**Shard System**

>**@usage**

>```ts
>const shard = new Aoijs.ClientShard(bot:Bot,mainfile:string,options?: ShardOptions)

>**@events**

>```diff
>+shard.onShardReady 
>+shard.onShardResume
>+shard.onShardDisconnect
>+shard.onShardError
>+shard.onShardReconnecting 

>**@cmds**

>```diff
>+shardReadyCommand
>+shardResumeCommand
>+shardDisconnectCommand
>+shardErrorCommand 
>+shardReconnectingCommand 



-----
## Functions 
### Error Objects 
>**Error Messages Now Work For Both Normal , Parser Objects and Full Object Mode**

>```diff
>//normal mode 
>
>+$onlyIf[1==2;error occured{newEmbed:{title:hi}}]
>
>//parser object mode 
>
>+$onlyIf[1==2;{"content":"error","embeds":"{newEmbed:{title:hi}}","components":"{actionRow:{button:Error:danger;error}}"]
>
>//full object mode
>
>+$onlyIf[1==2;{"content":"hi","embeds":[{"title":"hi"}],"components":[{"type":1,"components":[{"label":"Error","type":2,"style":4,"customId":"error"}]}]}]
>
### Utility Functions 
>```diff
>-$abbreviate[number]
>+$abbreviate[number;decimal?]
### Calling Functions 
#### Emoji Functions 
>```diff 
>-$addEmoji[name;url;returnEmoji?;RoleId;RoleId;...]
>+$addEmoji[guildId;Name;url;returnEmoji?;reason?;roleId;roleId;...]
>
#### Components Functions
>```diff
>//addButtons 
>+$addButton[index;label;style;customId/url;disabled?;emoji?]
>//addSelectMenu 
>+$addSelectMenu[index;customId;placeHolder;minValue?;maxValue?;options;options;...]
>//awaitComponents
>-$awaitButtons[messageId;userfilter;customId,customId,...;awaitedCommand,awaitedCommand,...;errorMsgContent?,errorMsgEmbed?,errorMsgFlag?;uses?]
>+$awaitComponents[messageId;userfilter;customId,customId,...;awaitedCommand,awaitedCommand,...; Embed-errors?or ErrorObject?;uses?;data?]
#### Message Functions 
>```diff
>-$sendMessage[message;returnId?]
>+$sendMessage[content;embeds?;components?;files?;sticker?;allowedMentions?;messageReference:mentionTheUser?;returnId?]
>
>-
##### Embed Functions 
>```diff
>-$addField[name;value;inline?]
>+$addField[index;name;value;inline?]
>
>+$addFields[index;name:value:inline?;name:value:inline?;...]
>
>-$addTimestamp[timestamp?] | $addTimestamp 
>+$addTimestamp[index;timestamp?] | $addTimestamp[index] 
>
>-$author[name;iconUrl?;url?]
>+$author[Index;Name;iconUrl?;url?]
>
>-$color[hex|int|RANDOM]
>+$color[index;hex|int|RANDOM]
>
>-$description[Text]
>+$description[Index;Text]
>
>-$footer[Text;iconUrl?]
>+$footer[Index;Text;iconUrl?]
>
>-$image[url]
>+$image[Index;url]
>
>-$thumbnail[url]
>+$thumbnail[Index;url]
>
>-$title[Text;url?]
>+$title[Index; Text;url?]

