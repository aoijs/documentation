---
description: >-
  Prunes members from the guild based on how long they have been inactive, by
  kicking them.
---

# $pruneMembers

This function kicks all inactive members without roles and with optional given roles from the given guild, if they were inactive for at least the given amount of days.

Raw usage: `$pruneMembers[amount of days(optional);guildID(optional);reason (optional);roleid1:roleid2:roleid3... (optional)]`

#### Options:

* `amount of days` =&gt; Number of days of inactivity required to kick 
  * optional
  * must be between 1 and 30
  * defaults to 7
* `guildID` =&gt; the guildID the members should be checked for prune status 
  * optional
  * defaults to current guildID
* `reason` =&gt; reason that would be shown in the Audit-Log 
  * optional
  * defaults to "none"
* `roles` =&gt; Array of roles to bypass the "...and no roles" constraint when pruning so it includes members with given roles in the prune status 
  * optional
  * separated by colons

#### Example Command:

This example kicks all inactive members without roles they have been inactive on Discord for at least 30 days and all inactive members with my two given roles with the reason "Too many members".

```text
bot.command({
name: "prunestatus",
code: `
Pruning would kick:
$pruneMembers[30;$guildID;too many members;741266432574357586:820666519331405854] members!
`
})
```

