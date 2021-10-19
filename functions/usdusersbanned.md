# $usersBanned

This function returns the list of banned users from the current server with optional seperator sorted by userID/mention or usernames.

Default return are usernames of the banned users. The default separator is `,`

Raw usage:`$usersBanned[id/mention/username (optional);separator (optional)]`

#### Example:

```js
bot.command({
name: "ban-list",
code: `
List of banned users:
$usersBanned[username;, ]
`
})
// Returns all banned users sorted by their username separated by a comma.
```

> ℹ️ Keep the 2,000 character limit in mind. 

> ℹ️ If your server has many bans, use functions like [$cropText](functions/usdcroptext.md) to stop after 2,000 chars or [$createFile](functions/usdcreatefile.md) to send the full list in a text file.

