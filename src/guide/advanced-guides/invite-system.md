# Invite System

## Introduction

A feature everyone has been asking for. An invite tracker system to track invites by users.

## How to enable

To enable the system, simply write in

```javascript
const Aoijs = require('aoi.js')
const bot = new Aoijs.Bot({
token: "token",
prefix: "!",
fetchInvites: true
})
```

Make sure you enable `SERVER MEMBERS` intents

![](../../.gitbook/assets/image%20%2844%29.png)

## Functions

With the invite tracker system, of course there's the functions!

### $userInfo

This function gets the user's invite information

```javascript
$userInfo[option;userID (optional)]
```

#### Options

* inviter - The user who invited the author/specified user
* code - The invite code the inviter used
* real - The count of users the author/specified user invited that are still in the server
* fake - The count of alt accounts \(Discord Age 10 Minutes and below\) the author/specified user invited \(Alt Account also must leave the server to be counted\)

```javascript
bot.command({
name: "invites",
code: `
$title[$username's invite info]
$thumbnail[$authorAvatar]
$description[
Total: $sum[$userInfo[real];$userInfo[fake]]
Real: $userInfo[real]
Fake: $userInfo[fake]
---------------------
Invited By: $userTag[$userInfo[inviter]] (\`$userInfo[code]\`)]
`
})
```

### $resetInvites

This function resets the invites the specified user has OR the whole guild \(if no user specified\)

```javascript
$resetInvites[guildID;userID (optional)]
```

```javascript
bot.command({
name: "resetInvites",
code: `
Successfully reset invites for $username[$mentioned[1]]
$resetInvites[$guildID;$mentioned[1]]
`
})
```

