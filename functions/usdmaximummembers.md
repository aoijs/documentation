# $maximumMembers

This function returns the limit of members the given guild has. This is only for large servers with more than 100,000 members. All guilds below return 100000.

Raw usage: `$maximumMembers[guildID (optional)]`

#### Usage:

Example command to return the amount of maximum members of the current guild:

```js
bot.command({
name: "maxmembers",
code: `
Limit: $maximumMembers
`
})
```

Example command to return the amount of maximum members of the another guild:

```js
bot.command({
name: "maxmembers",
code: `
Limit: $maximumMembers[773352845738115102]
`
})
```

