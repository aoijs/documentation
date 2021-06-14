---
description: Returns an amount of members that can be pruned.
---

# $pruneStatus

This function shows you how many inactive members without roles and with optional given roles can be pruned currently from the given guild without actually kicking them..

Raw usage: `$pruneMembers[amount of days(optional);guildID(optional);roleid1:roleid2:roleid3... (optional)]`

#### Options:

* `amount of days` =&gt; Number of days of inactivity required to kick 
  * optional
  * must be between 1 and 30
  * defaults to 7
* `guildID` =&gt; the guildID the members should be checked for prune status 
  * optional
* `roles` =&gt; Array of roles to bypass the "...and no roles" constraint when pruning so it includes members with given roles in the prune status 
  * optional
  * separated by `:`

#### Example Command:

```text
bot.command({
name: "prunestatus",
code: `
Pruning would kick:
$pruneStatus[5;$guildID;741266432574357586:820666519331405854] members!
`
})
```

