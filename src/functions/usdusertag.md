---
description: Gets specified user ID's username and discriminator easier
---

# $userTag

This function returns the users username AND tag 

```text
$userTag[userID (optional)]
```

Lets find the authors tag

```javascript
bot.command({
name: "userTag",
code: `
$userTag 
`
})
// Would return username#discriminator
```

Now lets find Kubaturis tag

```javascript
bot.command({
name: "userTag",
code: `
$userTag[$findUser[Kubaturi]] 
`
})
// Would return Kubaturi#0001
```

And of course, `$userTag[$message]` will work

