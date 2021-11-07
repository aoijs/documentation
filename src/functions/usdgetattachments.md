---
description: Gets attachment info of the provided Message.
---

# $getAttachments

With this function you can get information about message attachments, e.g. the name or url of an image.

Raw usage: `$getAttachments[channelid;messageid;position;properties]`

#### Properties:

* `name` => the name of the attachment
* `id` => the attachment ID
* `url` => the url of tha attachment (e.g. image url)
* `size` => the size of the file/image
* `width` => the width of the attachment

#### Example Command:

```
bot.command({
name: "get-file",
code: `
$getAttachments[$channelID;838701159710720001;1;name]
`
})
```

![Example usage to get the image name of a message's first attachment.](<../../.gitbook/assets/image (15).png>)
