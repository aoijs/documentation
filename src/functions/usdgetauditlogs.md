---
description: Returns audit log information.
---

# $getAuditLogs

With this function you can check Audit Log entries. Every field is optional. Action field defaults to everything, user field to everyone.

Raw usage: `$getAuditLogs[limit;userID;action;guildID;format]` 

#### Format option:

Format is an optional field where you can customize the response of the bot. Here you can use the following options to replace each with it's audit log response:

* `{executor.username}` =&gt; username who triggered the audit log 
* `{executor.tag}` =&gt; username and discriminator of the user that executed the audit log 
* `{executor.id}` =&gt; userID of the user that triggered the audit log entry
* `{executor.mention}` =&gt; mention of the user that executed the audit log entry 
* `{target.id}` =&gt; the id of the target \(can be a channel/message/user id or the guild id\) 
* `{action}` =&gt; see list below.

#### Action Filter:

You can use the options at the bootom of the page to filter the audit logs:

* ALL
* GUILD\_UPDATE 
* CHANNEL\_CREATE
* CHANNEL\_UPDATE
* CHANNEL\_DELETE
* CHANNEL\_OVERWRITE\_CREATE
* CHANNEL\_OVERWRITE\_UPDATE
* CHANNEL\_OVERWRITE\_DELETE
* MEMBER\_KICK
* MEMBER\_PRUNE
* MEMBER\_BAN\_ADD
* MEMBER\_BAN\_REMOVE
* MEMBER\_UPDATE
* MEMBER\_ROLE\_UPDATE
* MEMBER\_MOVE
* MEMBER\_DISCONNECT
* BOT\_ADD
* ROLE\_CREATE
* ROLE\_UPDATE
* ROLE\_DELETE
* INVITE\_CREATE
* INVITE\_UPDATE
* INVITE\_DELETE
* WEBHOOK\_CREATE
* WEBHOOK\_UPDATE
* WEBHOOK\_DELETE
* EMOJI\_CREATE
* EMOJI\_UPDATE
* EMOJI\_DELETE
* MESSAGE\_DELETE
* MESSAGE\_BULK\_DELETE
* MESSAGE\_PIN
* MESSAGE\_UNPIN
* INTEGRATION\_CREATE
* INTEGRATION\_UPDATE
* INTEGRATION\_DELETE

#### Example Command:

Simple usage without optional fields:

```text
bot.command({
name: "audit-logs",
code: `
Last audit log entries:
$getAuditLogs
`
})
```

Example command to filter last 5 bans and list their mentions:

```text
bot.command({
name: "audit-logs",
code: `
Last audit log entries:
$getAuditLogs[5;everyone;$guildID;MEMBER_BAN_ADD;<@!{target.id}>]
`
})
```

