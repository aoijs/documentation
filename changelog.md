---
description: aoi.js - changelog from previous versions and latest.
---

# Changelog

## aoi.js - 5.0.8
### Added/Fixed

- Added await to interactions
- Added missing async in $interactionDefer
- Fixed createObject overwriting the d.data
- Fixed map and $onlybotperms still give an error if the bot has admin but not particular perms in cache
- Fixed $emojiCount
- Fixed $globalUserLeaderboard
- Fixed timestamp for custom number
- Fixed $awaitMessage timeout error and custom timeout in $timeoutMember

## aoi.js - 5.0.7
### Added/Fixed

- Added $memberAvatar[userId?;size?;dynamic?;format?]
- Added $timeoutMember
- Added $expandNumber
- Added pre defined data transfer from cmd to awaitedCmd in $loop
- Added allowedmentions field in $interactionReply[content;embed?;components?;files?;allowedMentions?;ephemeral?]
- Updated $author src code
- Dynamized the type part of $emojiCount
- Bumped djs version
- Repositioned the error message in $newTicket
- Fixed var name in $closeTicket
- Fixed nonPrefixed executing all Cmds which dont have aliases when user types undefined
- Fixed createVoiceAdapter is not a function in $guild
- Fixed various bugs.
- Removed ms completely

## aoi.js - 5.0.6
### Added/Fixed

- Added $oldMsgData support messageDelete event
- Added $slashOption => $slashOption[option name]
- Added $oldMsgData => $oldMsgData || $oldMsgData[options]
- Added support for functions in name property of interactionCommand
- Added support for v4 if in customFunctions
- Added missing defines in $rawLeaderboard
- Added createdAt createdTimestamp and json data
- Added permissions property in Role()
- Updated $botLeave , $boostingSince src code from v4 to v5
- Updated all ResetVar functions src code from v4 to v5
- Fixed data transfer from main cmd to awaited Cmd in $if when {execute} is used
- Fixed typo in $sendTTS
- Fixed memberExist return true for empty args
- Fixed $setUsername
- Fixed $allMembersCount
- Fixed missing functions outdated
- Removed extra require('fs') in parserjs
- $suppressErrors only execute once when multiple functions give error -
- Interaction stop the code execution when one function gives error
- $message[args] return values [for Selectmenu] and options value [for slashCommands]
- $msg field optional in $newTIcket
- Lavalink returns correct songInfo title
- Lavalink shuffle fixed.
- Improvements to src.

## aoi.js - 5.0.5
## Added/Fixed
>```diff
>+Added awaits strict checking of banners
>+Fixed commands.js only executing alwaysExecute
>+Changed dependencies (upcoming for Music

## aoi.js - 5.0.4
### Added/Fixed

>```diff
># Misc Changes
>+Added awaits to add required functions
>+Renamed package to src
>+Formatted class and handler folder
>+Added missing guild Data in messageDelete Event
>+Changed default content from '' to ' ' , now you can use {newEmbed:} directly in functions like $editIn etc..
>+Updated message data send operation (errorMessage)
>+Updated Error Handling messages
>+Updated component incorrect field data
>+Updated entire src format
>+Fixed presence operator
>+Fixed EmbedData of icon user
>+Fixed typos
>+Fixed activities error
>+Fixed allowedMentions in Intepreter
>+Changed forEach -> for
>
># Bot Class Changes
>+rateLimitCommand()
>+onRateLimit()
>+webhookUpdateCommand()
>+onWebhookUpdate()
>
># Function Changes
>+Added $awaitData[option]
>+Added $lavalinkexecute[shuffle]
>+Added line to convert number strings to number in condition, now  >= and <= should work
>-$ServerEmojis[guildId?]
>+$serverEmoji[separator?;guildId?]
>-$authorBanner 
>+$authorBanner | $authorBanner[size?;dynamic?;format?]
>+added support for aliases in $commandInfo
>+Fixed typo in $forEachGuildChannel
>+Fixed $math (finally)
>-$getUserBanner 
>+$getUserBanner | $getUserBanner[userId;size?;dynamic?;format?]
>-$createServerInvite[channelId;options...]
>+$createServerInvite[guildId;options...]
>+$createChannelInvite[channelId;otpions...]
>-$modifyCHannelPErms[roleId/userId;channelId;guildId;perms;perm;perm;...]
>+$modifyCHannelPErms[roleId/userId;channelId;perms;perm;perm;...]
>+endAwaitCmd for all forEach function
>+Fixed $randomText returning only value of one randomText even if fields are different
>-$randomString[range]
>+$randomString[range;diffExec?]
>+Fixed $awaitCmdReactions
>+Fixed $argsCheck not stoping the execution 
>+Fixed $getLeaderboardInfo
>+Fixed get vars returning [Object object] for object type data
>+Fixed $moveUser
>+Fixed $awaitMessages
>+Fixed $awaitCmdReactions
>+Fixed $awaitComponents
>+Fixed $banCount
>+Fixed lavalink volume / data

## aoi.js - 5.0.3
### Added/Fixed

- Added $rawLeaderboard,
- New Usage => $rawLeaderboard[variable;order?;type?;customResponse?;list;page?] //returns leaderboard without checking if the id is valid type, good for when you don't have server member privileged intent
- Added guildId in $getCustomStatus,
- New Usage => $getCustomStatus[userID?;guildId?;type?]
- Added buffer support to $attachment,
- New Usage => $attachment[attachment;name;url/buffer]
- Added v4 $if support for cmds and can be switched by Adding $if : 'v4' in Command
- Added $deleteIn in interpreter
- Added $setRolePosition
- Added $readyTimestamp
- Added $isChannelManageable
- Added $isRoleEditable
- Added $isSelfdefeaned
- Added $isSelfMuted
- Added $isServerMuted
- Added $isServerDeafened
- Added $isStreaming
- Added $isVideoIn
- Added custom type support in $createApplicationCommand
- Added global support in $deleteApplicationCommand
- Added updatesChannel,systemChannel,ruleChannels in $guild
- Added $rolePosition
- Added Type Protection on Vars
- Added guildCommand option in $fetch
- Added $reverse
- Added helpers in interpreter
- Added dapi support for parsers
- Added customDb support for Leaderboard functions
- Added $isTicket
- Added auto fetch to $getApplicationCommandId/options
- Added direct channelID support for all callbacks
- Added $disableMentionType
- Fixed $newTicket and Added guildId support,
- New Usage => $newTicket[name;msg;categoryId/guildId?;returnId?;errorMsg?]
- Fixed $getUserBadges
- Fixed blacklist system for dm
-Fixed OnMessageDelete() callback
- Fixed $role
- Fixed $platform
- Fixed $userRoles
- Fixed $getCooldownTime returning NaN
- Fixed $jsonRequest crashing for customError
- Fixed $math
- Fixed removedRoles property for $oldMember
- Fixed $deleteWebhook
- Fixed $setStatus
- Fixed $userRoleColor
- Fixed requiring Perms in $modifyChannelPerms
- Fixed $hasPermsInChannel
- Fixed $if returning false message
- Fixed $SuppressErrors
- Fixed $argsCheck
- Fixed $closeTicket for customDb
- Fixed $usersWIthRole
- Fixed $componentCollector
- Fixed $awaitMessages
- Fixed $reactionCollector triggering for the bot
- Fixed $old/newApplicationCmd
- Fixed $old/newChannel
- Fixed $old/newEmoji
- Fixed $old/newGuild
- Fixed $old/newMember
- Fixed $old/newRole
- Fixed $old/newState
- Fixed $deleteIn / $editIn
- Changed disabledMentions to allowedMentions in interpreter
- Changed database.js for more generalised database menthods
- Changed $messageSlice second field from required to optional
- Removed $lerefImages
- Removed forced [] in $interactionDelete

## aoi.js - 5.0.2
### Added/Fixed

- Fixed has functions
- Made onlyif and other conditional function optional content
- Added $date
- Changed $day to return day instead of number
- Changed $month to return month in string instead of number from 0 to 11
- Changed $channelType to return lowercase type(like in v4)
- Fixed $if to allow message without {execute}
- Added catch error to $kick
- Fixed $mentionType
- Fixed CustomDB to CustomDb
- Fixed $ban
- Changed $wait to have n16 promised timeout
- Changed $updateCommands to async
- Added `catch error` to interaction functions
- Fixed ClearInterval to clearInterval
- Fixed $randomstring infinitely recursive loop
- Added await to this.getGUild in this.findId
- Added {interaction} option
- Fixed {edit} not working in normal mode
- Fixed $highestRole and $hoistedRole
- Fixed Blacklist System to work in Dms
- Added $deleteApplicationCommand
- Added presence and countBots in $membersCount
- Fixed $charCount
- Fixed $awaitMessages ms is not defined error
- Fixed $updateCommands not working fot windows file system
- Changed data in deletemessage callback to get full data
- Fixed $oldMessage
- Fixed $math
- Added `nonPrefixed`
- Added `( , )` , `&&` and `||` to escapes

## aoi.js - 5.0.1
### Added/Fixed

- Fixed lavalink incorrect constructor
- Fixed $numberSeparator
- Fixed `ComponentParser` emoji part (now it supports name, id, animated too)
- Fixed $allMembersCount
- Fixed $addTimestamp
- Fixed $Image bracket
- Fixed all `randomId` type functions
- Fixed reactionRemoveEmoji using inviteCreate event
- Fixed $getVar functions not returning default value
- Fixed $onlyBotPerms and $onlyPerms
- Fixed `setCode` returning ' ' instead of '' for undefind values
- Fixed $findTextSplitIndex
- Fixed $readfile, $renamefile and $writefile
- Fixed errorMessage needs forced content
- Fixed $wait
- Fixed nonPrefixed
- Fixed respondToBots
- Fixed $argcheck error msg
- Fixed wrong `scope` in $getBotInvite
- Fixed alwaysExecute
- Fixed webhookId
- Fixed guild Data
- Fixed $channelCount
- Fixed $banCount
- Added args to $djsEval
- autoWarning is re-enabled
- Added force to fetch Functions
- Added more `optional` fields in $httpRequest


## aoi.js - 5.0.0
### Environment Changes 
>```diff
>- Nodejs version 12.x
>+ Nodejs version >=16.6.1 
### Package Changes 
#### Class Changes 
## Bot 
**@options**

* ***ADDITION***
>```diff
>+cache
>+database
>+events
>+intents 
>+respondOnEdit
>+suppressAllErrors
* ***CHANGES***
>```diff
>- errorMessage : "message"
>+ errorMessage : ["content","embed","components","files"]
>```
* ***DELETION***
>```diff
>-fetchInvites
>- boosterToken
>- databasePath 
>- db 
>- disableFunctionStarting 
> **[List Of All Properties And Their Description](../options/botOptions.md)**
**@events**

* ***ADDITION*** 
>```diff
>+bot.onStickerCreate
>+bot.onStickerUpdate
>+bot.onStickerDelete 
>+bot.onThreadCreate
>+bot.onThreadUpdate
>+bot.onThreadDelete
>+bot.onThreadListSync
>+bot.onThreadMemberUpdate
>+bot.onThreadMembersUpdate 
>+bot.onMemberAvailable
>+bot.onMembersChunk 
>+bot.onReactionRemoveAll
>+bot.onReactionRemoveEmoji 
>+bot.onStageInstanceCreate
>+bot.onStageInstanceCUpdate
>+bot.onStageInstanceDelete 
>+bot.onGuildUnavailable 
* ***CHANGES***
>```diff
>-bot.onJoined 
>+bot.onJoin 
* ***DELETION*** 
>```diff
>-bot.onFunctionError 
**@commands**

* ***ADDITION*** 
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
* ***DELETION***
>```diff
>-bot.loadCommands
>-bot.musicStartCommand
>-bot.musicEndCommand 
>-bot.createLavalinkConnection
## Voice 
**@options**

* ***ADDITION***
>```diff
>+client
>```

**methods**
>```diff
>+ Voice.joinVc(voicechannel,textchannel)
>```
## LoadCommands
 **@method**
>```diff
>+ LoadCommands.load(cmd manager,path,debug)
>+ LoadCommands.update(debug)
>+ LoadCommands.setColor(theme)
>```
## Lavalink
  **@methods**
>```diff
>Lavalink.createLavalinkConnection(url,pass,debug,secureProtocol)
>```
----------
## FunctionChanges
* ***ADDITION***
>```diff
>+$awaitComponentsUntil[channelId; messageId; userFilter; time; customIds; awaitCommands; errorMsg?; data? ]
>+$awaitMessageReactions[channelId;messageId;filter;time;reactions;commands;errorMsg?;data?]
>+$addButton[index;label;style;customId;disabled?;emoji?]
>+$addFields[index;name:value:incline?;...]
>+$addSelectMenu[index;customId;placeHolder;minValue;maxValue;disabled;options;options;...] //options => label:description:value:default?:emoji?
>+$addThreadMember[channelId;threadId;userId;reason?]
>+$authorAccentColor[def?]
>+$authorBanner[size?;dynamic?;format?]
>+$bottyping
>+$broadCastEval[function]
>+$blacklist[type;id;id;id;..] //for user type first id is guildId
>+$blacklistError[type;errorObject]
>+$blacklistOnlyCommands[cmd name;cmd name;....]
>+$createStageInstance[ channelId;topic;privacy?]
>+$createSticker[guildid;url;name;returnSticker?;tags?; description?;reason?]
>+$createThread[ channelId;name;archive?;type?;startMessage?;returnId?]
>+$createCache[type;name]
>+$deleteChannel[channelId]
>+$deleteEmoji[emoji]
>+$deleteSTicker[guildId;stickerId]
>+$deleteThread[channelId;threadId]
>+$disableMentionType[type]
>+$eventData[property]
>+$eventEmit[eventname;data;data;...]
>+$fetchActiveThreads[ channelId;option;...]
>+$fetchArchivedThreads[ channelId;option;...]
>+$fetchClientValues[property]
>+$findInCache[ type;name;prop;value;findType?;returnValue?]
>+$fetch[ method ;query ]
>+$forEachRole[ guildId,time,awaitData,...cmds ]
>+$getUserAccentColor[user;def?]
>+$getUserBanner[userId;size?;dynamic?;format?]
>+$getCacheData[type;name;option?]
>+$interactionDefer
>+$interactionDeferUpdate
>+$interactionFollowUp[content;embeds?; components?;files?;ephemeral?]
>+$interactionUpdate[content;embeds?; components?;files?]
>+$invite[option]
>+$isButtonInteraction
>+$isCommandInteraction
>+$isComponentInteraction
>+$isContextMenuInteraction
>+$isSelectMenuInteraction
>+$isCustomEmoji[emoji]
>+$isInteger[number]
>+$isUnicodeEmoji[emoji]
>+$joinThread[channelId;threadId]
>+$killShard[shardId]
>+$leaveThread[channelId;threadId]
>+$newApplicationCmd[option]
>+$nonEscape[message]
>+$oldApplicationCmd[option]
>+$reactionData[option]
>+$removeThreadMember[channelId;threadId;userId;reason?]
>+$respawnAllShards
>+$spawnShard[shardId]
>+$shardGuilds[shardId;sep?]
>+$shardPing[shardId]
>+$setCacheData[type;name;value]
>+$tempCooldown[ time;id;errorObject? ]
>+$guildChannels[guildId?,option?,sep?]
>```

* ***CHANGES***
>```diff
>-$awaitCmdReactions[filter,time,reactions,commands,errorMsg?]
>+$awaitCmdReactions[filter,time,reactions,commands,errorMsg?,data?]
>
>-$awaitButtons[messageID,userFilter,customIDs,cmds,errorMsg?,uses?]
>+$awaitComponents[messageID,userFilter,customIDs,cmds,errorMsg?,uses?,data?]
>
>-$awaitMessages[channelId,userFilter,time,replies,cmds,errorMsg?,dm?]
>+$awaitMessages[channelId,userFilter,time,replies,cmds,errorMsg?,data?,dm?]
>
>-$addTimestamp[timestamp?]
>+$addTimestamp[index;timestamp?]
>
>-$apiMessage[channelId,content,embeds?,components?,reply?,returnId?]
>+$apiMessage[channelId,content,embeds?,components?,files?,stickers?,allowedMentions?,reply?,returnId?]
>
>-$author[name;iconUrl?;url?]
>+$author[index;name;iconUrl?;url?]
>
>-$activity[id?]
>+$activity[id?;guildId?]
>
>-$authorAvatar
>+$authorAvatar[size?;dynamic?;format?]
>
>-$complexCooldown[type;time;error?]
>+$advanceCooldown[time;id;error?]
>
>-$ban[userID, reason?, days?]
>+$ban[userId, guildId?, days?, reason?]
>
>-$botTyping[timeout]
>+$botTyping
>
>-$changeNickname[ userId,nick ]
>+$changeNickname[ userId,nick,reason ]
>
>-$channelSendMessage[channelId;message;returnId?]
>+$channelSendMessage[channelId;errorObject;returnId?]
>
>-$color[color]
>+$color[index;color]
>
>-$createSlashCommand[ guildId,name,description,...opts? ]
>+$createApplicationCommand[ guildId,name,description,defaultPermission?,type?,...opts?]
>
>-$createChannel[name, type?, returnID?, parentID?]
>+$createChannel[guildID, name, type?, returnId?, parentId?]
>
>-$createRole[name, color?, mentionable?, hoisted?, position?, ...perms?]
>+$createRole[ guildId,name,color?,hoist?,position?,mentionable?,... permissions?]
>
>-$getServerInvite[guildid?]
>+$createServerInvite[ channelId?, ...options?]
>
>-$createWebhook[ channel,name,avatar?,returnW?, seperator?]
>+$createWebhook[ channel,name,avatar?, seperator? ]
>
>-$cpu
>+$cpu[type?]
>
>-$eval[code;returnCode?]
>+$eval[code;returnCode?;sendMessage?;returnData?;returnId?]
>
>-$footer[text;iconUrl?]
>+$footer[index;text;iconUrl?]
>
>-$forEachChannel[...cmds ]
>+$forEachChannel[ time,awaitData,...cmds ]
>
>-$forEachGuild[...cmds ]
>+$forEachGuild[ time,awaitData,...cmds ]
>
>-$forEachGuildChannel[...cmds ]
>+$forEachGuildChannel[time,awaitData,...cmds ]
>
>-$forEachMember[...cmds ]
>+$forEachMember[ time,awaitData,...cmds ]
>
>-$forEachUser[...cmds ]
>+$forEachUser[ time,awaitData,...cmds ]
>
>-$getEmbed[channelId;messageId;option]
>+$getEmbed[channelId;messageId;index;option]
>
>-$getSlashCommandId[ name , type? ]
>+$getApplicationCommandId[ name , type? ]
>
>-$getSlashCommandOptions[name, guildID?]
>+$getApplicationCommandOptions[name, guildID?]
>
>-$getChannelVar[var;Id?]
>+$getChannelVar[var;Id?;table?]
>
>-$getGlobalUserVar[var;Id?]
>+$getGlobalUSerVar[var;Id?;table?]
>
>-$getMessageVar[var;Id?]
>+$getMessageVar[var;Id?;table?]
>
>-$getServerVar[var;Id?]
>+$getServerVar[var;Id?;table?]
>
>-$getUserVar[var;Id?;guildId?]
>+$getUserVar[var;Id?;guildId?;table?]
>
>-$highestServerRole
>+$highestGuildRole
>
>-$interactionReply[content;embed?;components?;flag?;type?]
>+$interactionReply[content;embed?;components?;files?;ephemeral?]
>
>-$interactionEdit[content?;embeds?, components?]
>+$interactionEdit[content?;embeds?, components?,files?, allowedMentions?]
>
>-$if[condition]
>-code
>-$endif
>+$if[condition;true message;false message] //use {execute:} to execute an awaitedCommand
>
>-$kick[userId;reason?]
>+$kick[userId;guildId?;reason?]
>
>-$lowestServerRole[guildiD?]
>+$lowestGuildRole[guildId?]
>
>-$loop[times;cmds...]
>+$loop[times;awaitData;cmds...]
>
>-$botping
>+$messagePing
>
>-$modifySlashCommand[guildID, commandID, name, description, ...opts]
>+$modifyApplicationCommand[guildID, commandID, ...data]
>
>-$modifyRole[roleID,name,color,hoisted,mentionable]
>+$modifyRole[guildId, roleId, ...roleDatas]
>
>-$modifyWebhook[webhookID, webhookToken, name, avatar]
>+$modifyWebhook[webhookId, name, avatar, channelId = d.channel?.id, reason]
>
>-$nickname[userId?]
>+$nickname[userId?;guildId?]
>
>-$pruneMembers[days?, guildId?, roleIds?, reason?, count?]
>+$pruneMembers[days = 7, guildId?, roleIds?, dry? , reason?, count?]
>
>-$reactionCollector[messageID,userFilter,time,reactionOrReactions,commandOrCommands,removeReactions?]
>+$reactionCollector[channelId, messageId, userFilters, time, reactions, awaits, removeReaction?, awaitData?, endAwait?]
>
>-$reply[messageId;message;mentionTheUser?]
>+$reply[messageId?, mentionUser?]
>
>-$ram
>+$ram[type?]
>
>-$resetGlobalUserVar[varname]
>+$resetGlobalUserVar[varname, table?]
>
>-$resetServerVar[varname]
>+$resetServerVar[varname, table?]
>
>-$resetUserVar[varname]
>+$resetUserVar[varname, table?]
>
>-$random[lowerLimit;upperLimit;decimal?]
>+$random[lowerLimit;upperLimit;decimal?;diffExec?]
>
>-$replaceText[text;replacer;replacedTo]
>+$replaceText[text;replacer;replacedTo;how much?]
>
>-$resolveColor[r, g, b, toHex?, type?]
>+$resolveColor[type, returnAs?, ...datas]
>
>-$roleExists[roleId]
>+$roleExists[roleId, guildId?]
>
>-$roleId[roleResolver]
>+$roleId[roleResolver, guildId?]
>
>-$colorRole[roleID, color]
>+$setRoleColor[roleID, color]
>
>-$setChannelVar[varname, value,Id?]
>+$setChannelVar[varname, value,Id?;table?]
>
>-$setGlobalUserVar[varname, value,Id?]
>+$setGlobalUserVar[varname, value,Id?;table?]
>
>-$setMessageVar[varname, value,Id?]
>+$setMessageVar[varname, value,Id?;table?]
>
>-$setServerVar[varname, value,Id?]
>+$setServerVar[varname, value,Id?;table?]
>
>-$setTimeout[ duration, timeoutData, pulse?]
>+$setTimeout[name, duration, timeoutData, pulse?]
>
>-$setUserVar[varname, value,Id?]
>+$setUserVar[varname, value,Id?;table?]
>
>-$setVar[varname, value]
>+$setVar[varname, value;table?]
>
>-$takeRole[ userId,roleId ]
>+$takeRole[ guildId,userId,roleId ]
>
>-$takeRoles[userId,roleId ]
>+$takeRoles[ guildId,userId,roleId;;... ]
>
>-$thumbnail[url]
>+$thumbnail[index;url]
>
>-$title[text;url]
>+$title[index;text;url]
>
>-$unban[userID,reason?]
>+$unban[userId, guildId?]
>
>-$uptime
>+$uptime[ option? ]
>
>-$userAvatar[userId?, size?, dynamic?]
>+$userAvatar[userId?, size?, dynamic?;format?]
>
>-$userPerms[userId,sep?]
>+$userPerms[userId?, sep?, guildId?]
>
>-$userRoleColor[ userId]
>+$userRoleColor[ userId?,guildId? ]
>
>-$userRoles[userId, option?;sep?]
>+$userRoles[userId?, guildId?, option?,sep?]
>
>-$userRolesCount[userId?]
>+$userRolesCount[userId?, guildId?]
>
>-$usersBanned[option?, sep?]
>+$usersBanned[guildId?;force?, option?, sep?]
>```

* ***DELETION***
>```diff
>-$authorMessage
>-$awaitReactions
>-$awaitReactionsUntil
>-$blacklistID
>-$blacklistRoleID
>-$blacklistServerID
>-$botLastMessageChannelID
>-$botLastMessageID
>-$createCollection
>-$deleteCollectionKey
>-$disableChannelMention
>-$disableEveryoneMention
>-$disableRoleMention
>-$emoijiID
>-$emojiName
>-$emojiToString
>-$filtermessageWords
>-$findCollectionKey
>-$getCollectionKey
>-$inviteChannelID
>-$inviteMaxUses
>-$inviteCode
>-$inviteGuildId
>-$inviteURL
>-$inviteUserID
>-$inviteUses
>-$ms
>-$packageName
>-$randomMentions
>-$serverRegion

* ***Misc***
>updated Parsers
>
>new interpreter
>
>executionTime can be used in embed
>
>new managers
>
>new classes

* ***NOTE*** 
> music will be added in later update along with the functions that are missing and are not in deletion section
> 
## aoi.js - 4.6.0

### Changes

* $playSong improved
* Lavalink Fixes (musicStart, musicEnd support, queue fixed, etc)
* Fixed $apiMessage target id
* Fixed $numberSeparator decimal
* musicEnd callback works immediately $playSong is triggered
* $songInfo: `duration`, `current_duration`, `duration_left` will no longer (time) seconds only `MS`
* Fixed {target.id} returning logs id instead of the target users id 
* Removed useless clutter in src
*$skipTo should now work 
* Removed $skipTo deleting songTitle's
* Fixed $complexCooldown globalUser


## aoi.js - 4.5.0

### Added

* Added $isChannelManageable\[channelID\]
* Added $isVideoOn\[userID\]
* Added $isStreaming\[userID\]
* Added $isServerDeafened\[userID\]
* Added $isServerMuted\[userID\]
* Added $isSelfDeafened\[userID\]
* Added $isSelfMuted\[userID\]
* Added $readyTimestamp
* Added $setRolePosition\[roleID;newPosition\]
* Added $isRoleEditable\[roleID\]

  Improvements

* Added 5 new properties in $guild \("ownerid", "nsfwlevel", "joinedtimestamp", "joinedat", "afktimeout",\)
* Added “different Execution” method in $random
* Added $packageName
* Added colorful logging for Command Handler
* Added Initialized aoi.js colorful.

### Removed

* Fixed buttoncollector and awaitButtons sending error message when 2 users execute it at same time
* Fixed $modulo
* Fixed $formatDate
* Fixed $msg 
* Fixed Client disconnecting when switch VC’s with Music
* Fixed interactionCommands name
* Fixed await.js msg ID
* Fixed main\_scheme\_1.sql log when using variables delete will no longer appear
* Removed useless client Options
* Removed unneeded interpreters
* Removed Booster API \(should have been removed\)
* Some formatting been made

## aoi.js - 4.4.4

### Added / Fixed

* Added $removeLinks\[text\] - Removes links from the provided text.
* Added $removeNumbers\[text\] - Removes numbers from the provided text.
* Added $removeNewLines\[text\] - Removes all new lines from the provided text.
* Added $rulesChannelID\[\(optional\) guildID\] - Returns the server's rules channel ID.
* Added $suppressEmbeds\[messageID;channelID\] - Suppresses embedded content from a message.
* Added $unsuppressEmbeds\[messageID;channelID\] - Unsuppresses embedded content from the embed-suppressed message.
* Added $shardCount - Returns how many shards the Client has.
* Added $removeSpecialChars\[text\] - Removes special characters from the provided text.
* Added New properties in $msg: webhookid, issystem, type, istts, editedtimestamp, editedat, iscrosspostable
* Added connectedBots in Client Option. \(This connect to API to check how many Clients use aoi.js\)
* Cleanup / format functions.
* $playSong defean works as intended.
* $playSong no longer returns now playing.
* Connecting to API is false by default. \(connectedBots\)
* Removed $lerefImages
* Added missing Client Options in TypeScript declarations.

## aoi.js - 4.2.1

### Fixed / Improved

* Forced ms to be installed as dependency.
* Minor changes.

## aoi.js - 4.2.0

### Added / Fixed

* New Error system, \(:x: no longer exist\) 
* Remove not needed if statements in functions, 
* Interaction commands have been change to using client API. 
* Fixed {edit} 
* Fixed typo in functions. 
* Fixed several functions, 
* Added `SuppressAll / errorMessage` Client Option

## aoi.js - 4.0.2

### Fixed / Improved

* Improved logging to Console 
* Updated `ytdl-core` dependency _music works_
* Updated README.md
* Updated package description
* Updated `index.js` prefix string.

## aoi.js - 4.0.1

### Added

* Added functions support in interactionCommand which uses client in src code

  you can now use $ban with buttons,

* Added aliases \(yes/no\) for {field} in apiMessage

### Fixed / Improved

* Fixed ComponentParser 
* Fixed actionRow duping on using more than 1 actionRow
* Fixed ErrorParser but now whole field has to be used

  for example {author:hi} won't work but {author:hi::} will

  \(note this is only for apiMessage , buttonCollector and awaitButtons

  \(because they operate on Discord API\)

* Fixed Interaction type in interactionCommand handler which earlier made buttonCollector and awaitButtons not usable in V4
* Fixed $creationDate \(again\)
* Changed parse-ms version \(2.0.0\)

## aoi.js - 4.0.0

### Added

* $apiMessage: "sends a message using Discord api - $apiMessage\[content,embed \(optional\), components \(optional\), reference \_message\_id:mention the replied user\(default false\); Return id \(optional default no\)\]", 
* $awaitButtons: "awaits buttons for given amount of uses - $awaitButtons\[msgid;userfilter; customID, customID,...; awaitcommand, awaitedcommand,...; error content,Error embed,erorr flags \(optional\);uses \(optional : default 1\)\]",
* $buttonCollector: "creates a collector for given customIDs;$buttonCollector\[messageID;everyone/userID;time;customID,customID,...;awaitedcommand,awaitedcommand,...;error msg content,error msg embed,error msg flags \(64 for ephemeral\) \(optional\); awaitedcommand \(executes when collector ends\)\(optional\)\]", 
* $interactionEdit:"edits the original interaction Response - $interactionEdit\[content;embeds; components\]", 
* $interactionDelete:"deletes the original interaction Response \(doesn't support ephemeral messages\)" $interactionReply\[content;embeds; components \(optional\);flags \(optional\);type \(optional\)\] been improved

### Fixed / Improved

* Fixed reactionAddCommand 
* Fixed $vcSize 
* Improved $creationDate 
* Improved $isNumber
* Fixed functionError not emit. 
* **REMOVED** `Ready on Client ...` **YOU MUST USE bot.readyCommand callback.**

## aoi.js - 3.0.0

### Added / Improved

* Added : Function Error Callback System bot.onFunctionError\(\) bot.functionErrorCommand\(\)
* $handleError\[error options\] options: { function: "returns the function that threw error", command: "returns the command that threw the error", error: "Error message that was thrown by the function" }
* Added : Variable Callbacks System bot.onVariableCreate\(\) bot.variableCreateCommand\(\)
* bot.onVariableUpdate\(\) bot.variableUpdateCommand\(\)
* bot.onVariableDelete\(\) bot.variableDeleteCommand\(\)
* $oldVariable\[variable options\] $newVariable\[variable options\]
* Added Application Command Callbacks
* bot.onApplicationCmdCreate\(\) bot.applicationCmdCreateCommand\(\)
* bot.onApplicationCmdUpdate\(\) bot.applicationCmdUpdateCommand\(\)
* bot.applicationCmdDeleteCommand\(\)
* $oldApplicationCmd\[application options\]
* $newApplicationCmd\[application options\]
* Added : $serverLeaderboards\[variable;asc/desc\(optional\);custom response \(optional\);list \(optional\);page\(optional\)\] 
* Added : $vcSize\[options;guildID/all\(optional\)\] // default is current guild options:{ channels : "number of voice channels bot is in", users:"number of users in same voice channels as of bot", song:"number of tracks in the queue of the bot" }
* Changed : $getSlashCommandOptions\[\] // added Global Support
* Fixed : $fileSize\[\] , updated the math so it can be more accurate 
* Fixed: $getAttachments\[\] fixed the src code error 
* Fixed : $messageSlice : was giving errors if args was blank
* Added : client.aoi.options \( will get all the options that were provided in "new aoi.Bot\({...}\)"\)
* Added : applicationCache options in Client Class which can be turned on by doing "applicationCache : true" in "new aoi.Bot\({...}\)"
* Added : caching system for slash commands
* Added : client.applications.slash \( to get collection of cached cmds\)
* working of caching system :

  _Global slash cmds are cached on starting the bot_

  _guild Slash gets cached when they are using or are updated /created_

  _new global and guild Callbacks get cached when they are created /Updated_

  _when a slash cmd is deleted the data of the cache of that slash cmd is also delete from the "client.applications.slash"_

* Added ephemeral embed support in slash
* Changed discord api version to V9 in client.\_api //Note: d.\_api still uses V8 so that people can also use V8 if they want
* Added : $writeFile\[file;data; encoding \(optional\)\] // write a new data in the new data or add new data with existing one 
* Added : $renameFile\[old file name, new filename\] 
* Added : $readFile\[filename\]

## aoi.js - 1.0.6

### Fixed

* Fixed DBH Error Installation

## aoi.js - 1.0.5

### Added

* Added [$isEveryoneMentioned ](../functions/usdiseveryonementioned.md)by Der Bond\#0001
* Added [$mentionedRolesCount](../functions/usdmentionedrolescount.md) by Der Bond\#0001
* Added [$mentionedUsersCount ](../functions/usdmentioneduserscount.md)by Der Bond\#0001
* Added [$mentionedChannelsCount](../functions/usdmentionedchannelscount.md) by Der Bond\#0001
* Added [$maximumMembers](../functions/usdmaximummembers.md) by Der Bond\#0001
* Added [$defaultMessageNotifications](../functions/usddefaultmessagenotifications.md) by Der Bond\#0001
* Added [$variablesCount](../functions/usdvariablescount.md) by Der Bond\#0001
* Added 5 missing [Permissions](../guide/begin/permissions.md) by Der Bond\#0001
* Added [$sendTTS](../functions/usdsendtts.md) by Ayaka\#2043
* Added [$fileSize](../functions/usdfilesize.md) by Ayaka\#2043
* Added [$getAttachments](../functions/usdgetattachments.md) by Ayaka\#2043
* Added [$getAuditLogs](../functions/usdgetauditlogs.md) by blox\#8880
* Added [$pruneStatus](../functions/usdprunestatus.md) by blox\#8880
* Added [$pruneMembers ](../functions/usdprunemembers.md)by blox\#8880
* Added [$nodeVersion](../functions/usdnodeversion.md) by blox\#8880

### Fixed

* Fixed $sendMessage errored when only 1 field was given
* Fixed Lavalink TimeState
* Fixed $addReactions slow and incorrect inputs
* Fixed $channel
* Fixed $clientToken
* Fixed $randomEmoji
* Fixed $multi

### Updated

* Added {tag} placeholder for $globalUserLeaderboard by Blox\#8880
* Added optional guildID field for $customEmoji
* Added Support for Global and Ephemeral Support for Slash Commands by Ayaka\#2043

## aoi.js - 1.0.1

### Added

* Added [$clientToken](../functions/usdclienttoken.md)
* Added [$randomEmoji](../functions/usdrandomemoji.md)
* Added [$uri](../functions/usduri.md) by RAKE\#6882

### Fixed

* Fixed $splitText
* Fixed $multi

### Updated

* Updated $userLeaderboard, [$allEmojiCount](../functions/usdallemojicount.md), and $emojiCount by Blox\#8880
* Updated some [$client](../functions/usdclient.md) options by Pranav\#1758

## DBD.JS - 3.0.6

### Added

* Added $resolveColor\[Red; Green; Blue;toHex \(optional\) \(yes/no\)\], convert's rgb color into hex or color number. 
* Added new code for $userExists to use cache if user exist in cache, else it will use fetch. 
* Added $complexCooldown\[type;time;errorMessage\] 
* Added $isValidImageLink\[url\] 
* Added $mfaLevel or $mfaLevel\[guildID\] 
* Added `fvalue` \(field value\) option in $getEmbed 
* Added $parseTime\[time\] 
* Added $joinVC\[Voice Channel ID\] 
* Added $leaveVC 
* Added `separator` field in $serverNames

### Fixed

* Fixed $findUser and $findMember keeps returning "undefined" when the given data is a whitespace / empty. 
* Fixed $resetGlobalUserVar 
* Cleaned $voiceID code. 
* Cleaned $userAvatar code. 
* Fixed separator not working in $rolePerms 
* Removed code's for $user to not use the author of message if id is invalid, instead it return errors. 
* Fixed `;` escaping to `:`

## 3.0.5

### Fixed

* Fixed $username cant detect brackets if its empty 
* Fixed $reset variables functions 
* Fixed $getLeaderboardInfo \(almost forgot\) 
* Fixed $ordinal \(why no one reported this smh\) 
* Fixed `ms` option in $getCooldownTime returning `MINUS` timestamp 
* $volume now won't break if the specified volume is `0` 
* Fixed Lavalink executing more than 1 `musicEnd` event Relocated `$lavalinkExecute` function to `handlers` folder 
* Cleared unnecessary variables and code's for $findUser and $findMember Database speed has improved \(options\) 
* **Removed `ffmpeg-static` as dependency**

## 3.0.2

### Added

* Added $client compact function

### Fixed

* Fixed $guildRoles 
* Fixed voiceStateUpdate callback returning error db is not defined
* Fixed $userPerms
* Fixed $activity not detecting brackets 
* Fixed $userTag 
* Fixed $randomText
* Fixed $removeTextSplitElement 
* Fixed $toLocaleUppercase 
* Fixed $newTicket
* Fixed $isEmoji 
* Fixed $setTimeout 
* Fixed $isValidHex 
* Fixed $findTextSplitIndex
* Fixed $getCooldownTime - user now must provide the cooldown time in the first field of $getCooldownTime

## 3.0.1

### Fixed

* Fixed $botOwnerID 
* Fixed $customEmoji 
* Fixed $divide 
* Fixed $deleteIn 
* Fixed $reboot 
* Fixed $toLowercase 
* Fixed $toUppercase 
* Fixed $isNumber 
* Fixed $skipTo 
* Fixed `cannot read property 'value' of undefined` in onLeave callback when fetchInvites is set to true 
* Fixed $author when there is $authorID in front of it 
* Fixed Booster API 
* Fixed $resetUserVar 
* Fixed $resetServerVar 
* Fixed $resetGlobalUserVar 
* Fixed $randomText 
* Fixed `cannot read property 'value' of undefined` in onBanAdd callback when fetchInvites is set to true 
* Fixed $membersCount

## 3.0.0

### Added

* Added bracket supoort to $cloneChannel 
* Added $modifyEmoji\[emojiID;name;...roles \(optional\)\] 
* Added $resolveEmojiID\[emoji string / name / id\] 
* Added $exec\[command line\] 
* Added $addObjectProperty now supports adding object values to the main object.. 
* Added $hasPermsInChannel\[channelID;userID;...perms\] 
* Added $modifyRolePerms\[roleID;+perm;-perm;...\] you can also use +all or -all \(self-explanatory\) 
* Added $getBanReason\[userID;guildID \(optional\)\] 
* Added $isBanned\[userID;guildID \(optional\)\] 
* Added $awaitCmdReaction\[filter/everyone;time;reaction1,reaction2,...;command1,command2,...;error message \(optional\)\] 
* Added $filterMessageWords\[text;caseSensitive \(yes/no\);...words\] 
* Added $$map\[text;splitter;awaited command;separator \(optional\)\] you can use {value} in the awaited command to get the value of each element in the array that's being mapped 
* Added $serverPreferredLocale / $serverPreferredLocale\[guildID\] - Added $serverAvailable / $serverAvailable\[guildID\] 
* Added $awaitReactionsUntil\[channelID;messageID;userFilter/everyone;time;reaction1,reaction2,...;count1,count2,....;command1,command2,...;error \(optional\)\] 
* Added $concatTextSplit\[text;separator\] 
* Added $textSlice\[text;x;y \(optional\)\] 
* Added $indexOf\[text;char\] 
* Added $textTrim\[text\] 
* Added $mentionType\[argument\] 
* Added $categoryChannels\[channelID;option \(count/name/id/mention\);separator \(optional\)\] 
* Added return amount `(yes or no)` field in $clear 
* Added `howMany` field in $replaceText default to -1 
* Added $mutualServers or $mutualServers\[userID;separator \(optional\)\] 
* Added $cropText\[text;limit;charToSplit \(optional\);append \(optional\)\] 
* Added $httpRequest\[url;method \(optional\) \(default to GET\);body \(optional\);property \(optional\) \(if response is json\);error \(optional\);headerName:headerValue \(optional\);headerName:headerValue \(optional\);...\] 
* Added $hoistedRole or $hoistedRole\[userID\]  
* Added $createVar\[varName:varValue;varName:varValue;...\]  
* Added $deleteUserVar\[variable;userID \(optional\);guildID \(optional\)\] 
* Added $deleteGlobalUserVar\[variable;userID \(optional\)\] 
* Added $deleteServerVar\[variable;guildID \(optional\)\] 
* Added $deleteChannelVar\[variable;channelID \(optional\)\] 
* Added $deleteMessageVar\[variable;messageID \(optional\)\] 
* Added channel type `stage` in $createChannel 
* Added typescript declarations \(happy typescript user noise\) woo! 
* Added $lavalinkExecute\[method;...data\] 
* Added createLavalink\(url, password, debug \(default to false\)\) 
* Added `database` option in bot constructor, making it possible to use custom database with dbdjs.db-like api

### Callbacks

```text
Bot.onRateLimit()
Bot.rateLimitCommand()

$rateLimit[rateLimitOption]
```

```text
Bot.onVoiceStateUpdate()
Bot.voiceStateUpdateCommand()

$oldState[voiceStateOption]
$newState[voiceStateOption]
```

```text
Bot.onMemberUpdate()
Bot.memberUpdateCommand()

$newMember[memberOption] 
$oldMember[memberOption]
```

### Changes

* Fixed small issue with Bot.deletedCommand 
* Fixed same issue in Bot.updateCommand 
* Fixed $dateStamp 
* Error messages handler has been modified a bit to make $channelSendMessage and other functions sending a message to a different channel work as expected with every {} function 
* Fixed $getUserBadges returning undefined errors on specific users 
* Fixed $findUser... for non cached 
* $platform now returns none if it points to the client user 
* Fixed $addCmdReactions throwing non customized errors 
* Fixed Update Warning to `api.leref.ga` instead of old API url.
* Fixed $abbreviate return NaNundefined if the specified number is 0 
* Changed $let and $get from using global client.variables scope to using local interpeter scope 
* $jsonRequest now use axios 

#### **Interpeter Changes**

* Allows data to change object variable 
* Changed let object; to let object = data.object \|\| {};

**Custom Event Changes**

* Deleted $eventData 
* Event data will be available in $djsEval\[d.object.eventdata\] 
* Rewritten invite tracker system to support new db 
* Fixed $blackListRoleIDs returning error message is not defined 
* Made sure tube.js doesn't interfere with ffmpeg when pre-events are ongoing

#### **Important Changes**

`$description[[Text\\](Link)] must be $description[[Text](Link)]` _It works like how it should have been intended from before_

## 2.2.6

### Fixed

* Fixed Console API Same Error

## 2.2.5

### Added

* Added $formatDate\[datestamp / milliseconds / stringed date \(Example: $creationDate\)/ ISO String; Format\] Almost a full coverage of `moment` format, syntax of formats can be found in [https://momentjs.com/docs/\#/parsing/string-format/](https://momentjs.com/docs/#/parsing/string-format/) 
* Added $humanizeMS\[MS;Show Limit;Separator\] - Converts Milliseconds into a Readable duration. 
* Added `Connected to API` will reconnect to API if disconnected. 
* Added $let - Assigns data to a temporary variable that can be changed and retrieved later in the command. Similar to variables. 
* Added $get - Returns data from the $let function. 
* Added new filed `useFilter`, Default is `yes`, if set to `no`, it will use first found instead of filtering first for $playSpotify

### Changes

* Fixed $log returning error. 
* Improved $reboot \(Closes DB Properly\)
* Rewritten $playSpotify System 
* Removed show success field in $playSpotify 
* $playSoundCloud is now using [https://api.leref.ga/](https://api.leref.ga/), if its down, you know who to contact to.
* $playSpotify Loads more stable instead of Huge request in one second. Also plays the first song while loading songs in the background \(Could result a glitchy sound in the process\).

## 2.2.0

### Added

* Added guildID and returnCount field in $cacheMembers 
* Added `{username}` `{discriminator}` and `{usertag}` custom param and `current (yes or no) (optional)` field. 
* Added $disableEveryoneMentions 
* Added $abbreviate\[number;decimalPlace\] 
* Abbreviate provided number
* $channel\[channelID;option\] 
* $emoji\[emojiID;option\]
* $guild\[guildID;option\]
* $msg\[channelID;messageID;option\] 
* $role\[roleID;option\] 
* $user\[userID;option\]
* $webhook\[hookURL;option\] 
* $isEmoji\[content\] - Returns true/false 
* $ordinal\[number\] - Returns the number in ordinal format.

### Improved

#### bot.loadCommands\(\)

bot.loadCommands\(path, debug?\) are now more advanced Allowing subfolder inside subfolder:

```text
..economy
....auto
......daily.js
....manual
......work.js
..moderation
....auto
......tempmute.js
....manual
......mute.js
```

Allowing other command type \(default to normal\):

**Example**

```javascript
module.exports = {
  channel: '773364744240496640',
  code: `Welcome $userTag !!`,
  type: 'joinCommand'
}
```

Allowing multiple commands:

**Example**

```javascript
module.exports = [{
  channel: '773364744240496640',
  code: `Welcome $userTag !!`,
  type: 'joinCommand'
}, {
  name: 'ping',
  code: `Pong! $pingms`
}]
```

### Changed

* Fixed `cannot read property 'delete' of undefined` when the bot start and `fetchInvites` are set to `true` - 
* Fixed $playspotify returning error in command 
* Fixed Music Handler to not cause potential memory leak \(Running On More Servers\) 
* Fixed $numberSeparator doesn't work on some platform 
* Fixed $guildID returning Error in Direct Messages instead of empty value. 
* Fixed $findServerChannel not being able to find servers with \[\] in names 
* Fixed $disableRoleMentions disables all mentions
* Fixed and Improved $jsonRequest 
* $playspotify now using the format `artist name - song name` while searching for the video 
* $isValidHex now more accurate

## 2.1.1

### Added

* Added $channelOverwrites or $channelOverwrites\[channelID;{mention} \({type}\):\nAllowed Perms: {allow}\nDenied Perms: {deny};separator\]
* Added $disableChannelMentions

### Changes

* Improved $playSpotify to now follow the song order in playlist
* Fixed $reply not being able to ping roles
* Fixed $onlyIf and $checkCondition completely broken with 0 as value
* Fixed some issues in updateCommands handler
* Fixed both reactionAddCommands / reactionRemoveCommands handlers
* Removed request for next song info after a song playing, so reduce the chance to get rate limited

## 2.1.0

### Added

* Added {deletecommand} or {deletecommand:time} to embed errors 
* Added $getCooldownTime\[server/user/globalUser;command name;ID;return ms \(yes/no\) \(optional\)\] 
* Added nonprefixed commands to support aliases 
* Added hyperlink url field to $author
* Added $setCollectionKey\[collection name;key;value;deleteAfter \(optional\)\] 
* Added $getCollectionKey\[collection name;key\] 
* Added $createCollection\[collection name\] 
* Added $deleteCollectionKey\[collection name;key\] 
* Added $findCollectionKey\[collection name;key value;accurate \(optional\)\] 
* Added `last` or `>` option to $message and $noMentionMessage $noMentionMessage src code has been improved 
* Added $emojiExists\[emojiID\] 
* Added $serverEmojiExists\[emojiID\] 
* Added Bot.timeoutPulseCommand\(\) for timeout heartbeats 
* Added guildID field to $memberExists 
* Added $spliceTextJoin\[text;separator1;separator2;separator3;every \(optional\)\]
* Added $removeContains\[channelID;limit;word1;word2;...\] 
* Added $stringEndsWith\[message;text\] 
* Added deleteMessageUponReact field to $awaitReaction 
* Added $userReacted\[messageID;userID;emoji\] or $userReacted\[channelID;messageID;userID;emoji\] 
* Added $memberJoinPosition or $memberJoinPosition\[userID\] 
* Added $disableRoleMentions 
* Added $userRoleCount or $userRoleCount\[userID\] 
* Added $isMuted now checks if user is server muted too 
* Added $isDeafened now checks if user is server deafened too 
* Added $boostingSince or $boostingSince\[userID;ms/date \(optional\)\] 
* Added guildID field to $hasRole 
* Added $songInfo\[duration\] now using the format `00:00:00`

### Callbacks

**New Callbacks**

```javascript
Bot.loopCommand()
```

properties are `channe`l, `code`, `executeOnStartup` and `every` channel / executeOnStartup are not required

```javascript
Bot.onTypingStart()
Bot.typingStartCommand({
    channel: (optional), 
    code: ``
})
```

Added $setTimeout\[duration;timeout data;timeout heartbeat \(optional\)\] example:

```javascript
//Setting a timeout that will send a message to your dms after given time. 
bot.command({
    name: "remindme", 
    code: `You will be reminded with $messageSlice[1] after $message[1].
$setTimeout[$message[1];
userID: $authorID 
message: $messageSlice[1]]`
})
```

```javascript
bot.timeoutCommand({
    code: `$sendDM[$timeoutData[userID];$timeoutData[message]]`
})
```

**setTimeout won't reset upon Bot restart :\) and these can go above 21 days**

New command:

```text
bot.timeoutCommand()
```

uses `code` and `channel` property \(channel is optional\) New Function: $timeoutData\[property\]

### Changes

* * Fixed $messagePublish throwing invalid channel id all the time 
* Fixed Music functions with incorrect usage/error message 
* Fixed $queue again 
* Fixed $newTicket sending supposed ticket message in the wrong channel 
* Fixed emojis not working properly with $textSplit / $splitText 
* Fixed $addObjectProperty trying to convert strings into numbers 
* Fixed $title closing / ignoring after putting \[ 
* Fixed $memberExists not working properly 
* Fixed $suppressErrors not working anymore 
* Fixed `name` option not working properly in $playSpotify 
* Fixed $channelPermissionsFor not working properly when using channelID field 
* Fixed $advancedTextSplit not being able to split special symbols 
* Fixed $playSong blocking the main thread 
* Fixed color option not working in $getEmbed 
* Fixed Bot Leaving Voice Channel even if VC empty OR another user leaving VC. 
* Fixed $hasEmbeds 
* FIxed $onlyIf and $checkCondition not working properly with some values 
* Fixed $findChannel returning undefined errors 
* Fixed $reply 
* Removed duplicated event listener for voiceStateUpdate

## 2.0.0

### Added

* Added $moveSong\[from;to \(optional\)\] Move song in the queue from x position to z, or remove it from queue if z is invalid 
* headers field in $jsonRequest $jsonRequest\[url;property;error;headerName:headerValue;headerName:headerValue;...\] 
* Added spaces field in $getObject $getObject or $getObject\[spaces\] 
* Added $math\[value\], Example: $math\[\(2+7\)\*9\] 
* Added $channelCooldown\[time;error message\] 
* Added $timezone = Get current timezone / $timezone\[timezone\] = Set timezone
* Added a field for $day $day\[return day of the week \(optional\) \(yes/no\)\] 
* Added $moveUser\[userID;channelID \(optional\);reason \(optional\)\] Used to move user from a voice channel 
* Added $deafenUser\[userID;deafen \(yes/no\);reason \(optional\)\] Used to deaf user in voice channel 
* Added $muteUser\[userID;mute \(yes/no\);reason \(optional\)\] Used to mute user in voice channel
* Added more methods $editChannel\[channelID;categoryID/$default;name/$default;position/$default;nsfw/$default \(yes/no\);bitrate/$default;userLimit/$default;syncPermission \(yes/no\);reason \(optional\)\] 
* Added $setRoles\[userID;roleID;roleID;...\] 
* Added `leaveEmpty` \(yes/no\) in $playSong, $playSoundcloud, and $playSpotify make it leave vc if the voice channel is empty 
* Added $loopSong - Loop current song
* Added `{delete:time} {attachment:name.extension:url}` -`{attachment:name.extension:url}` can be used multiple times in embed errors now 
* Added $emojisFromMessage or $emojisFromMessage\[message;separator \(optional\)\] 
* Added $giveRole\[userID;roleID\]
* Added $takeRole\[userID;roleID\] 
* Added $lowestRole or $lowestRole\[userID\] 
* Added $lowestServerRole
* Added $highestServerRole 
* Added $serverDescription
* Added $userRoleColor or $userRoleColor\[userID\]
* Added $channelPermissionsFor\[userID\] or $channelPermissionsFor\[channelID;messageID\] 
* Added $usersTyping or $usersTyping\[channelID;username/mention/tag/id;separator\] 
* Added $userInfo\[option;userID \(optional\)\] To get user invites info 
* Added $resetInvites or $resetInvites\[guildID;userID \(optional\)\] To reset guild or user invites
* Added `yes/no` as a valid field for $findUser $findChannel $findServerChannel and $findMember _\(defaults to yes\)_ using no will output undefined if no match was found. 
* Added guildID field to $setUserVar and $getUserVar 
* Added {edit:duration:{new message}:{new message}:{...}} to embed errors 
* Added {suppress:yes/no} to suppress latest embed 
* Added every possible option for $getEmbed 
* Added Fields to $getBotInvite for Permissions, $getBotInvite\[admin;sendmessages;connect\] or $getBotInvite - Added ability to escape } 
* Added $seekTo\[Number in Seconds\] 
* Skip the amount of duration that the request want to skip, $seekTo\[10\] =&gt; 10 Seconds of Song Skipped 
* Added $hasAnyPerm\[permission1;permission2;...\] or $hasAnyPerm\[userID;permission1;permission2;...\] 
* Added `addreactions` to permissions 
* Added $botLastMessageID and $botLastMessageChannelID 
* Added $hasAnyRole\[roleID1;roleID2;...\] or $hasAnyRole\[userID;roleID1;roleID2;...\] 
* Added $messagePublish or $messagePublish\[messageID\] or $messagePublish\[channelID;messageID\] 
* Added `userID` field to $awaitMessages \(last field\), more info on the !commandlist $awaitMessages
* Added $botTyping\[duration\] 
* Added $queueStatus 
* Return the current queue status \(playing, paused, and idle\) 
* Added $loopStatus 
* Return the current queue loop status \(song, queue, and none\) 
* Added $isPrune - Wether or not the queue message is pruned 
* Added type `(buffer/url)` field in $attachment, if the type set to buffer then we can put the data image directly, instead of putting image url. 
* Added $serverExists\[guildID\] 
* Added $isTicket or $isTicket\[channelID\] 
* Added $roleMembersCount\[roleID\]
* Added `current_duration` option in $songInfo\[option\] 
* Added a filter to delete Unavailable Videos `[Deleted video]` in a playlist 
* Added $songFilter\[type:value;type:value;...\] 
* Set an audio filter to current song 
* Added ability to disable functions when instantiating a dbdjs bot

```text
new dbd.Bot({ disabledFunctions: ["$botLeave", ...]
```

* Added $createFile\[Leref Mean;filename.extension\] 
* Added `{file:text:name.extension}` 
* Added $getChannelSlowmode or $getChannelSlowmode\[channelID\]

#### Invite Tracker System

To activate:

```javascript
new dbd.Bot({
 fetchInvites: true
})
```

and activate callbacks:

```text
- onJoined
- onLeave
- onInviteCreate
- onInviteDelete
- onBanAdd
- onGuildJoin
- onGuildLeave
```

* Added $userInfo\[option;userID \(optional\)\] - To get user invites info 
* Added $resetInvites or $resetInvites\[guildID;userID \(optional\)\] - To reset guild or user invites

### Callbacks

#### bot.onMusicEnd

```javascript
bot.musicEndCommand({
  channel: "$channelID",
  code:"Code"
})
```

### Custom Events

```javascript
//Bot setup
const event = require("events")
const Event = new event.EventEmitter()
const CustomEvent = Bot.createCustomEvent(Event)
CustomEvent.command({
name:"call", // A Name for the command, optional, atm it's needed but useless
listen:"emitted", // A listener that will be executed if the event was called/emitted
channel:"channel id", // a channel id to send the code
code:`Successful Emit was listened` //a code, yes
})
CustomEvent.listen("emitted") //Listen to emitted event and execute all commands that have "emitted" as the listen property
Also to get the data from event, you can use $eventData[property]
```

### Changed

* If Statement is now case insensitive
* Non-prefixed command is now case insensitive
* $alwaysExecute now working faster
* Updated $queue to not break after 323 songs.
* $clear now wont break if there is some 2 weeks old messages while bulk deleting
* Bot prefix is now case insensitive
* Fixed channelCreate / delete callbacks
* Fixed $isBoosting \(not really a fix, just a nullable checker\)
* bot.variables now can be used multiple times without removing the previous variables
* Fixed $addReactions \(if anything happens again it'll log the error\) and $addCmdReactions
* Fixed $forEach function
* Fixed $playSong characters not escaped: \[ and \]
* $djsEval can now be used multiple times
* Fixed some functions not working properly in awaited commands for $reactionCollector
* Fixed $disableMentions not working properly in normal commands
* Fixed Music Player crashing if $stopSong and $pruneMusic activated
* Fixed embed errors throwing undefined channel errors
* $jsonRequest doesn't use node-fetch anymore
* Changed $playSpotify search, it will filter videos that has the artists of spotify name
* Fixed $randomString
* $cpu is now more accurate
* $ram is now more accurate
* Fixed $random\[1;2\] always return 1
* Fixed $queue\[\] throwing split errors

### Escapable Characters

#### Added

* `:` Escape to `#COLON#`

#### Changed

* `;` Escape to `#SEMI#`

## 1.9.4

### Added

* Changed All Music Functions time default to `1s`
* `respondToBots` ignores webhooks too if it set to false \(normal commands\) 
* $alwaysExecute now ignores both bots and webhooks if `respondToBots` is set to false. 
* $messageFlags 
* $messageWebhookID
* Added error messages to $if functions \(these can't be suppressed\) 
* Added `duration_left` to $songInfo property

### Fixed

* Fixed $noMentionMessage 
* Fixed `botLoadCommands` 
* Fixed djsEval \(closing the code field after first semicolon\)

## 1.9.3

### Fixed

* Fixed Database not saving user/message input data. 
* Fixed Leaderboards 
* Fixed `get` errors. 
* Fixed botLeave callback

## 1.9.1

### Fixed

* Fixed installing error

## 1.9.0

### Renamed

* $getMessageAttachment =&gt; $messageAttachment 
* $userMessageID =&gt; $messageID 
* $unPinMessage =&gt; $unpinMessage 
* $typeOfMessage =&gt; $messageType 
* $sliceMessage =&gt; $messageSlice

### Added

* $serverNames 
* 2nd field in $djsEval 
* Added asynchronous: false/true \(default is true\) property to Bot.command setting to false will make the command not wait for other commands with same name to execute. 
* $executionTime 
* $allEmojiCount 
* Added $if, $else, $elseIf, $endelseIf and $endif, \(only $if appears on commandlist\) 
* Added inline field for error messages \({field}\) 
* Added 2nd field for $getCustomStatus $getCustomStatus\[userID;state/emoji\] 
* $findMembers\[query;limit \(optional\);{position} - {username} - {id} \(optional\);getID \(optional\)\] 
* $vanityURL 
* $vanityUses
* $replaceTextWithRegex\[text;regex;flags;new text\] 
* $getUserBadges now returns nitro classic and boosting badges \(depends\) 
* $updateCommands - update bot commands 
* $getObject - Returns a Stringified JSON Object of created/modified $createObject 
* $findChars\[string\] 
* $findNumbers\[string\] 
* $findSpecialChars\[string\] 
* {url:link} {timestamp:ms} for embed 
* $deleteMessage\[messageID\] or $deleteMessage\[channelID;messageID\] 
* $year 
* $month 
* $day 
* $hour 
* $minute 
* $second 
* $shuffleQueue 
* $queue doesn't need brackets anymore \($queue or $queue\[options\]\) 
* $botOwnerID or $botOwnerID\[separator\] 
* Added mobile property to client options:

```text
new dbd.Bot({ mobile: true })
```

* $volume return volume now 
* $allChannelsCount or $allChannelsCount\[type;type;...\] 
* $stringStartsWith\[message;text\] 
* $suppressErrors doesn't need brackets to leave empty Error 
* $clearReactions has been rewritten 
* Added `error` property to every Bot.\(command\) function error property is like code one, it'll be executed if the interpreter throws an error, and will execute the code in the error property if no error code was given, the error will be thrown to the console as normal 
* $error - the error that the interpreter threw

### Callbacks

```text
Bot.onPresenceUpdate()
Bot.onUserUpdate()

Bot.userUpdateCommand()
Bot.presenceUpdateCommand()

$oldPresence[presenceOption] - for presence update callback, returns old data
$oldUser[userOption] - for user update callback, returns old data
```

```text
Bot.onRoleDelete()
Bot.onRoleCreate()
Bot.onRoleUpdate()

Commands:
Bot.roleDeleteCommand()
Bot.roleUpdateCommand()
Bot.roleCreateCommand()

functions for these:
$oldRole[roleOption]
$newRole[roleOption]
```

```text
Bot.onChannelUpdate()
Bot.onChannelCreate()
Bot.onChannelDelete()

Commands:
Bot.channelDeleteCommand()
Bot.channelCreateCommand()
Bot.channelUpdateCommand()

Functions:
$oldChannel[channelOption]
$newChannel[channelOption]
```

### Fixed

* Bot.loadCommands\(path\) has been fixed 
* $allMembersCount no longer returns NaN if a guild is unavailable Fixed 
* $guildID\[name\] using id instead of name 
* Interpreter / functions are now case non sensitive Improved interpreter performance / speed 
* Fixed special symbols in $userTag Fixed 
* @discordjs/opus not installing when require again 
* Fixed $playSong parser returning error when one option. 
* Fixed $djsEval returning deleteBrackets is not a function 
* Fixed $reactionCollector again

## 1.4.0

### Added

* $eval now returns the rest of the code that was executed
* Added 2nd field to $eval
* You can now escape colons \(;\)
* Added url field to $title
* Added name field to $attachment
* $serverSplash or $serverSplash\[guildID;size \(optional\)\]
* Added channelID field to $editMessage
* $reply\[messageID;message;mention \(yes/no\)\]
* $sendCrosspostingMessage\[message;channelID;channelID;...\]
* $clear now allows any number \(100+\) on amount field IF the user filter is set to everyone
* $isValidLink\[url\] - true or false
* Added ms option to $creationDate and $memberJoinedDate
* Added emoji to $creationDate
* Added {error} to $suppressErrors

### Fixed

* Fixed special symbols for prefixes
* Fixed {reactions:} not working in $channelSendMessage
* $getLeaderboardInfo \(top option\) has been fixed
* Fixed $findServerChannel / $findChannel not able to find category names with uppercase letters
* $reactionCollector has been fixed \(fetches user if it's partial\)
* Fixed $numberSeparator not accepting 0

### Music

* Added $playSoundCloud\[url; soundcloud client\_id \(optional\);leave vc time;defean \(yes or no\);error message\] 
* Fixed unknown error with discordjs/opus. It will now force to install \(require\) 
* Removed clutter with Music, that cause Music to die in other guilds \(apparently it bugs if too much connections\) 
* Changed $playSong, $playSpotiy to Handler. 
* Allowed `time/defean` options. 
* Allowed more $songInfo options.
* $playSpotify will not download ReadableStream when searched

### Slash Commands

#### Event

```javascript
Bot.onInteractionCreate()
Commands:
Bot.interactionCommand({
name: "slash command name", 
code: "code to execute" 
})
```

#### Functions

* $getSlashCommandOptions\[name\] or $getSlashCommandOptions\[name;guildID\] 
* $createSlashCommand\[guildID;name;description;options \(optional\)\] 
* $modifySlashCommand\[guildID;commandID;name;description;options \(optional\)\] 
* $deleteSlashCommand\[guildID;name/id\] 
* $interactionReply\[message\]
* $getSlashCommandID\[name\] or $getSlashCommandID\[name;guildID\]

### DBH Support

```javascript
const bot = new dbd.Bot({
token: "TOKEN", 
prefix: "!",
dbhToken: "Token"
})
```

## 1.2.0

### Added

* $setChannelTopic\[channelID;topic\] \($setChannelTopic\[channelID\] removes channel topic\) 
* $modifyWebhook\[webhookID;webhookToken;name;avatar \(optional\)\] 
* $deleteWebhook\[webhookID;webhookToken\] - Added multiple embeds support to $sendWebhook 
* $sendWebhook\[webhookID;webhookToken;message;options...\]
* $getInviteInfo\[code/url;guildID/channelID/userID/isTemporary/expiresAt/createdAt/url/code/uses/maxUses\] 
* $pinMessage or $pinMessage\[channelID;messageID\] 
* $unPinMessage or $unPinMessage\[channelID;messageID\] 
* $channelCategoryID or $channelCategoryID\[channelID\] 
* $addMessageReactions\[channelID;messageID;reaction1;reaction2;...\] 
* $isUserDMEnabled or $isUserDMEnabled\[userID\]
* $unban now supports user name 
* $commandInfo\[command name;property\] 
* $advancedTextSplit\[text;split;index;split;index;...\] 
* $packageVersion 
* $isHoisted\[roleID\] 
* $isMentionable\[roleID\] 
* $isManaged\[roleID\] 
* $isValidHex\[hex or int\] 
* $addTimestamp now supports \[\] **-** $addTimestamp\[ms\] 
* $getLeaderboardInfo\[variable;id;user/globaluser/server;top/name/value\] - 
* $oldMessage - message update callback function

### Fixed

* aliases: "text" won't break anymore
* Fixed caps in command names & aliases
* Fixed $suppressErrors\[\] in await
* $message \(anything returning user's input\) is no longer executing embed errors

### Invite Functions

* $inviteUses
* $inviteURL
* $inviteCode
* $inviteGuildID
* $inviteChannelID
* $inviteUserID
* $inviteMaxUses
* $fetchInvites\[awaited command1;awaited command2;...\]

  \(NOT ASYNCHRONOUS\)

### Callbacks

* bot.onInviteCreate\(\) 
* bot.inviteCreateCommand\(\) 
* bot.onInviteDelete\(\) 
* bot.inviteDeleteCommand\(\) 
* bot.onBanAdd\(\) 
* bot.banAddCommand\(\) 
* bot.onBanRemove\(\) 
* bot.banRemoveCommand\(\) 
* bot.botJoinCommand\(\) 
* bot.onGuildJoin\(\) 
* bot.botLeaveCommand\(\) 
* bot.onGuildLeave\(\) 
* bot.onMusicStart\(\) 
* bot.musicStartCommand\(\)

### Music

* Fixed null when add songs to queue.
* Improved $playSpotify await system \(No longer takes 30s for 100 songs\)
* Better implementation to $playSong of ffmpeg.
* $playSong now support Youtube Playlists

## 1.1.0

### Added

* $serverBanner or $serverBanner\[guildID;size \(optional\);dynamic \(yes/no\)\(optional\)\]
* $isMentioned\[userID/roleID/channelID/everyone\] 
* $sendWebhook\[webhookID;webhookToken;message\] 
* $createWebhook\[channelID;name;avatar;returnWebhookID&Token \(yes/no\);separator\] - 
* $referenceGuildID
* $referenceChannelID
* $referenceMessageID
* $serverBoostCount
* Added missing permissions to the permission list 
* $newTicket\[ticket name;ticket message \(optional\);categoryID \(optional\);return ticket id \(yes/no\);error message \(optional\)\] 
* $closeTicket\[error message \(optional\)\]
* Allowed $random demicals \(yes/no\) - $playSong supports Youtube URL - 
* $createChannel now allows being created by category ID 
* $skipTo\[number\]
* $playSpotify\[url;show success \(number/name\);error message\]

### Fixed

* $ban is now able to ban users who are not in the Guild.
* Removed any unnecessary clutter in the package
* Skip/Next song no longer takes 5 seconds to load.
* Fixed Dispatcher disconnection issue.
* Improved speed and optimization
* No longer cache insanely for queue 

## 1.0.1

### Fixed

* ready.js bringing undefined

## 1.0.0

### Added

* $forEachGuild\[awaited command 1;awaited command 2;...\] 
* $forEachGuildChannel\[awaited command 1;awaited command 2;...\] 
* $forEachUser\[awaited command 1;awaited command 2;...\] 
* $forEachMember\[awaited command 1;awaited command 2;...\] 
* $forEachChannel\[awaited command 1;awaited command 2;...\] 
* $awaitMessages\[userID/everyone;time;reply1,reply2,...;command1,command2,...;error message\] 
* $cacheMembers 
* $findRole\[id/mention/name\] 
* $randomRoleID 
* $deleteEmojis\[emoji1;emoji2;...\] 
* $emojiCount 
* $serverEmojis 
* $serverRegion 
* $guildID\[guild name
* \] $setStatus\[text;type;status\] 
* $channelTopic or $channelTopic\[channelID\] 
* $typeOfMessage $modulo\[5;2\] 
* $findUser supports ID of users that don't share any server with the bot
* Bot.readyCommand\({ channel: "channel id", code: "code" }\)

### Music Changes

* Rewrote $loopQueue Should loop fully even only if 1 song 
* Fixed $skipSong not sending songInfo 
* Fixed $stopSong of dispatcher ending randomly 
* Fixed Dispatcher of UNDEFINED errors

### Fixed

* Fixed bug in $addEmoji 
* Fixed $guildID 
* $color has been fixed

## 0.6.5

### Added

* $isBanned\[userID\]
* $randomGuildID 
* $modifyChannelPerms\[channelID;+perm1;-perm2;/perm3;+perm4;...;roleID/userID\] 
* $slowmode\[channelID;time/0\] 
* $usersInChannel\[channelID;mention/id/username \(optional\);separator \(optional\)\] $activity returns "none" if the user has no current activities 
* $setBotAvatar\[url\] 
* $setBotName\[name\] 
* $djsEval now requires brackets \($djsEval\[code\]\) 
* $removeSplitTextElement\[index;index2;...\]
* $jsonRequest has been improved. You can now access to a property inside an object by using property1.property2 it also supports arrays. \[0\].property1 \(or just \[0\]? Up to the api ur using\) There are many other ways to use this, remember you have to escape \] though.
* $usersBanned or $usersBanned\[id/mention/username;separator \(optional\)\]
* $loopQueue

### Fixed

"Cannot send an empty message" log Removed quick.db from $loop / $textSplitMap $globalCooldown doesn't override variable values anymore

Fixed overwriting $skipSong - may not like hosts though..

## 0.6.0

### Added

* $getCustomStatus or $getCustomStatus\[userID\]
* $usersWithRole\[roleID;separator \(optional\);forceCaching \(yes/no\)\(optional\)\]
* Allowed mentions \($mentioned functions\) in $reactionCollector /
* $awaitReaction
* $onlyIfMessageContains\[text;word1;word2;...;error message\]
* $resetVar\[variable\]
* $resetGlobalUserVar\[variable\]
* $resetUserVar\[variable\]
* $resetServerVar\[variable\]
* $addObjectProperty\[key;value\]
* $createObject\[object string\]
* $getObjectProperty\[key\]
* $isValidObject\[string {}\]
* $sliceMessage\[from;to \(optional\)\]
* $colorRole\[roleID;hex or int color\]
* $randomUserID
* $randomMention
* $getMessage\[channelID;messageID;content/description/userID\]
* $randomChannelID
* $findServerChannel\[id/name/mention\]
* $findChannel is now global
* {image:url} to embed error messages
* $stopSong
* $skipSong
* $pauseSong
* $resumeSong

### Fixed

* $thumbnail
* $unban
* $reactionCollector, $awaitReaction

  \(They don't require quick.db anymore.\)

## 0.5.0 + 0.5.1

* Bot.reactionAddCommand\(\) \(channel and code properties\)
* Bot.reactionRemoveCommand\(\) \(channel and code properties\)

  Others: status property in Bot.status\(\)

* $onlyNSFW\[error message\]
* $sendDM\[userID;message\] 
* $suppressErrors\[message\] \(must go at the bottom\) 
* $onlyBotPerms\[perm1;perm2;...;error message\] 
* $userPerms or $userPerms\[userID;separator \(optional\)\] 
* $rolePerms\[roleID;separator \(optional\)\] 
* $cloneChannel or $cloneChannel\[channelID\] 
* $setGuildName\[new name\] 
* $setGuildIcon\[new icon\] 
* $deleteIn\[time\] 
* $setMessageVar\[variable;value;messageID \(optional\)\] 
* $getMessageVar\[variable;messageID \(optional\)\] 
* $emojiName 
* $emojiID 
* $emojiToString 
* $authorMessage 
* $argsCheck\[NUMBER/NUMBER;error message\] 
* $charCount or $charCount\[text\] 
* $authorAvatar 
* $creationDate\[guildID/userID/roleID/channelID;time/date \(optiona\)\] 
* $memberJoinedDate or $memberJoinedDate\[userID;date/time \(optional\)\] 
* $djsEval 
* $getEmbed\[channelID;messageID;title/footer/description/color/...\] 
* $getMessageAttachment 
* $filterMessage\[message;lettersOrSymbols\]  
* $getBotInvite 
* $getRoleColor\[roleID\] 
* $hasRole\[userID;roleID\] 
* $isBot or $isBot\[userID\] 
* $uptime 
* $lop\[output\] 
* $blackListServerIDs\[serverID;serverID;...;error message\] 
* $blackListIDs\[userID;userID;...;error message\] 
* $blackListRoleIDs\[roleID;roleID;...;error message\] 
* $voiceID\[userID\] 
* $status or $status\[userID\] 
* $attachment\[url\]
* $botLeave or $botLeave\[guildID\] 
* $botTyping 
* $userRoles or $userRoles\[userID;names/ids/mentions;separator\] 
* $onlyForServers\[serverID;serverID;...;error message\] 
* $round\[number\] 
* $truncate\[number\] 
* $dateStamp 
* $parseDate\[ms;date/time\] 
* $deleteChannels\[channelID;channelID;...\] 
* $createChannel\[name;type;return ID \(yes/no\)\]
* $cooldown, $globalCooldown, $serverCooldown using the old database.
* Some functions returning \[\] = breaking $onlyIf 
* $getServerVar not working in callbacks 
* $ is now escaping $ 
* $findUser

### Removed

* $reactionRoleAdd
* $reactionRoleRemove

## 0.4.0 + 0.4.1

### **Added**

* Fixed callbacks throwing errors
* Brackets are now escaped with \]
* $serverChannelExists
* $channelExists is now global
* $voiceID
* $channelUsed
* $deletecommand
* $onlyPerms\[perm1;perm2;error message\]
* $queue\[page;amount;custom queue\]
* $volume\[vol\]
* $queueLength
* $songInfo\[duration/userID/title/description/url\]
* $playSong\[url/name;error message\]
* $filterMessage\[text;charactersToRemove\]
* $djsEval \(global variable is d\)
* $userMessageID
* $checkCondition\[condition\]
* $editTextSplitElement\[index;new value\]
* $removeTextSplitElement\[index\]

### **Fixed**

* Fixed "variable not found" if the vars initial value is 0 or " "

## 0.2.0 + 0.2.1

### Added

* $setChannelVar\[variable;value\] or $setChannelVar\[variable;value;channelID\]
* $getChannelVar\[variable\] or $getChannelVar\[variable;channelID\]
* $setVar\[variable;value\]
* $getVar\[variable\]
* $checkContains\[message;text1;text2;...\] - returns true or false
* $serverFeatures or $serverFeatures\[guildID\]
* $highestRole or $highestRole\[userID\]
* $rolePosition\[roleID\]
* $getServerInvite or $getServerInvite\[guildID\]
* $userTag or $userTag\[userID\]
* $isBoosting or $isBoosting\[userID\] - returns true or false
* $randomString\[length\]

### Changed

* $textSplitMap, $loop and {execute:} now use awaited commands to execute.

### Removed

* _Ruben, forgot, to remove a file_

## 1.16

### **Added**

* $awaitReaction
* $attachment\[URL\]
* $clientID - Retrieves Bot ID.
* $reactionRoleRemove
* $reactionRoleAdd
* $reactionCollector

### Fixed

* $description\[\] - Offset acting weird, easy fix

### Removed

* Unnecessary junk, in the code.

## 0.1.0

### Added

* Custom Prefixes

  Bot.loadCommands\(path, debug\)

* Allowed $getServerVar\[prefix\] in `prefix:`
* Allowed Multiple Prefixes 
* $giveRoles
* $takeRoles
* $serverIcon
* $channelNSFW
* $onlyForIDs
* $membersCount\[\] `all;no` - can now allow or no Bots. 
* $addEmoji
* $findUser - Now Global \(Guilds\)
* $findMember - Per Guild
* $customEmoji - Actually Custom from all Guilds.
* $findRole
* $roleID
* $hasPerms
* $setGlobalUserVar
* $getGlobalUserVar
* $mentionedRoles
* $kick
* $botCount

### **Fixed**

* $membersCount\[\], returns offline, idle, etc.
* $getUserBadges, returning badges all uppercase, now properly lowercase.
* $addField works without $description

## 0.0.7

### Updated

* Readme with proper `bot` code

### Fixed

* Brackets in most function, to work without them
* Error Message properly

## 0.0.6

### Updated

* Readme with Bot Status!
