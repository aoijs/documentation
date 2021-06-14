# $webhook

This function returns the given webhook's specified property

#### Usage

This function has 2 fields

1. URL \(Required\)
2. Property \(Required\)

Raw Usage: `$webhook[URL;property]`

#### Options

* URL - The webhook's url the porperties are based off of
* Property - The property of the &lt;webhook&gt;

#### Available Properties

* name - Webhook's name
* id - Webhook's id
* token - Webhook's token
* avatar - Webhook's avatar URL
* created - Webhook's date and time of creation
* timestamp - How long ago the webhook was created
* url - Webhook's URL
* type - Webhook's Type
* exists - Whether or not the webhook exists, Returns Boolean
* guild - Webhook's guild of origin
* channelid - Channel of which the webhook is assigned to

```javascript
bot.command({
name: "webhook",
code: `
$webhook[https://discord.com/api/webhooks/793312378162642975/paNWUYLC22oL-t2hbYeu3zrwWXNfVxjn4TmDDVTISNVRbytCbptYM4DETJDTPzG-1JcA;name]
`
})

//Or specified webhook

bot.command({
name: "webhook",
code: `
$webhook[$message;name]
`
})
```

