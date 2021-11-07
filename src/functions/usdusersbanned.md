---
description: Returns a list of users that are banned from this guild.
---

# $usersBanned

This function returns the list of banned users from the current server with optional seperator sorted by userID/mention or usernames.

Default return are usernames of the banned users. The default separator is `,`

Raw usage:`$usersBanned[id/mention/username (optional);separator (optional)]`

#### Example:

```text
bot.command({
name: "ban-list",
code: `
List of banned users:
$usersBanned[username;, ]
`
})
// Returns all banned users sorted by their username separated by a comma.
```

{% hint style="info" %}
Keep the 2,000 character limit in mind. 

If your server has many bans, use functions like [$cropText](usdcroptext.md) to stop after 2,000 chars or [$createFile](usdcreatefile.md) to send the full list in a text file.
{% endhint %}

