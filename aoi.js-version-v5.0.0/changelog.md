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

> [You Can Check Those Properties In Details Here](../options/botOptions.ms)

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

##Lavalink
>**Lavalink has been Seperated into. a new class**

>**@usage**

>```ts 
>const lava = new Aoijs.lavalink(bot:Bot) ;
>lava.createLavalinkConnection(url: string,password:string,debug:boolean) 
