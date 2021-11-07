---
description: Returns the type of this message.
---

# $messageType

The type of the current message, e.g. DEFAULT. Here are the available message types:

* DEFAULT
* RECIPIENT\_ADD
* RECIPIENT\_REMOVE
* CALL
* CHANNEL\_NAME\_CHANGE
* CHANNEL\_ICON\_CHANGE
* PINS\_ADD
* GUILD\_MEMBER\_JOIN
* USER\_PREMIUM\_GUILD\_SUBSCRIPTION
* USER\_PREMIUM\_GUILD\_SUBSCRIPTION\_TIER\_1
* USER\_PREMIUM\_GUILD\_SUBSCRIPTION\_TIER\_2
* USER\_PREMIUM\_GUILD\_SUBSCRIPTION\_TIER\_3
* CHANNEL\_FOLLOW\_ADD
* GUILD\_DISCOVERY\_DISQUALIFIED
* GUILD\_DISCOVERY\_REQUALIFIED

#### Usage:

```text
bot.command({
name: "$alwaysExecute",
code: `
The server has reached boost level 3! 🎉
$onlyIf[$messageType==USER_PREMIUM_GUILD_SUBSCRIPTION_TIER_3;]
```

