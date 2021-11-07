---
description: Returns the size Of file in The project In the Provided Unit
---

# $fileSize

With this function you can check the size of the given file in your bot's host.

Raw usage: `$fileSize[file path;unit]`

#### Units:

* `b` =&gt; bytes
* `kb` =&gt; kilobytes \(1,000 bytes\)
* `mb` =&gt; megabytes \(1,000,000 bytes\)
* `gb` =&gt; gigabytes \(1,000,000,000 bytes\)

#### Example Command:

Using a file from the main folder to return it's size in kilobytes:

```text
bot.command({
name: "file-size",
code: `
$fileSize[server.js;kb]
`
})
```

Using a file from another folder to return it's size in megabytes:

```text
bot.command({
name: "file-size",
code: `
$fileSize[commands/moderation/anti_invite.js;mb]
`
})
```

{% hint style="info" %}
To use a file that's inside a folder, use it's path in the file path field like in the example above.
{% endhint %}

![example file path: commands/moderation/anti\_invite.js](../.gitbook/assets/image%20%2841%29.png)

