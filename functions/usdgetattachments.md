---
description: Gets attachment info of the provided Message.
---

# $getAttachments

With this function you can get information about message attachments, e.g. the name or url of an image.

Raw usage: `$getAttachments[channelid;messageid;position;properties]`  


#### Properties: 

* `name` =&gt; the name of the attachment
* `id` =&gt; the attachment ID
* `url` =&gt; the url of tha attachment \(e.g. image url\)
* `size` =&gt; the size of the file/image
* `width` =&gt; the width of the attachment

#### Example Command:

```text
bot.command({
name: "get-file",
code: `
$getAttachments[$channelID;838701159710720001;1;name]
`
})
```

![Example usage to get the image name of a message&apos;s first attachment.](../.gitbook/assets/image%20%2815%29.png)

