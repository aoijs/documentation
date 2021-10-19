# $roleMembersCount

This function will return the amount of users who have the given role using the role ID.

Raw usage: `$roleMembersCount[Role ID]`

Example:

```javascript
bot.command({
    name: "users",
    code: `
There are $roleMembersCount[773353338854572073] users with mod role in dbd.js
    `
})
```

> ℹ️ This count could not be exact, since this data is get from the cache and not the Discord API, this meaning if some user is not cached, the user will not count.

