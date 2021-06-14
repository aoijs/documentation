# $user

This function returns the given user's specified property

#### Usage

This function has 2 fields

1. User ID \(Required\)
2. Property \(Required\)

Raw Usage: `$user[userID;property]`

#### Options

* User ID - The user the properties are based off of
* Property - The property we're getting from &lt;user&gt;

#### Available Properties

* name - User's name
* id - User's ID
* tag - User's Tag
* discrim - User's discriminator
* mention - User's mention
* avatar - User's avatar URL
* isbot - Whether or not the user is a bot, Return's Boolean
* istyping - Whether or not the user is typing, Return's Boolean
* created - User's date and time of creation
* timestamp - How long ago the user was created
* lastmessageid - User's last message ID
* lastmessagechannelid - User's last channel ID

```javascript
bot.command({
name: "user",
code: `
$user[535566311942651924;name]
`
})

//Or specified user

bot.command({
name: "user",
code: `
$user[$mentioned[1];name]
`
})
```

