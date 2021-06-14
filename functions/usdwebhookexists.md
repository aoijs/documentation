---
description: Checks if a webhook exists
---

# $webhookExists

$webhookExists\[webhookID;webhookToken\]

This function checks if the given credentials lead to an existing webhook

```javascript
$webhookExists[webhookID;webhookToken]
```

Now lets use it

```javascript
bot.command({
name: "webhookExists",
code: `$webhookExists[793312378162642975;paNWUYLC22oL-t2hbYeu3zrwWXNfVxjn4TmDDVTISNVRbytCbptYM4DETJDTPzG-1JcA] 
` //This returns true
})

bot.command({
name: "webhookExists",
code: `$webhookExists[7934564363642975;paNWUYLC22oL-t2hnkldrneKLNFeklnUOknefwmOI34Ahgf] 
` //This returns false
})
/*
How to find your webhookID/Token
url: https://ptb.discordapp.com/api/webhooks/793312378162642975/paNWUYLC22oL-t2hbYeu3zrwWXNfVxjn4TmDDVTISNVRbytCbptYM4DETJDTPzG-1JcA
Your ID: 793312378162642975
Your Token: paNWUYLC22oL-t2hbYeu3zrwWXNfVxjn4TmDDVTISNVRbytCbptYM4DETJDTPzG-1JcA
*/
```

