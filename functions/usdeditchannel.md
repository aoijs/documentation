---
description: Edits channel properties.
---

# $editChannel

This function will allow you to modify a channel using the channel ID.

#### Fields

This function has 6 required fields:

1. Channel ID \(Required\)
2. Category ID \(Required\)
3. Name \(Required\)
4. Position \(Required\)
5. NSFW \(Required\)
6. Bitrate \(Optional\)
7. User Limit \(Optional\)
8. Sync Permission \(Required\)
9. Reason \(Optional\)

Raw usage: `$editChannel[channelID;categoryID/$default;name/$default;position/$default;nsfw/$default (yes/no);bitrate/$default;userLimit/$default;syncPermission (yes/no);reason (optional)]`

#### Options

* Channel ID - The channel we're editing
* Category ID - The category the channel is in
* Name - The channels name
* Position - The channels position
* NSFW - Whether or not the channel will be NSFW
* Bitrate -The bitrate of the voice channel
* User Limit - The limit of users to the voice channel
* Sync Permission - Whether or not the channel will sync perms
* Reason - The reason in the audit logs
* $default - This puts the property to the original/default option

#### Usage

```javascript
bot.command({
name: "edit",
code: `
Channel name modified!
$editChannel[$channelID;$default;$message;$default;$default;$default;$default;yes]
    `
})
```

