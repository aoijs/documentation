---
description: Retrieve the discriminator of the User.
---

# $discriminator

This function returns the users discriminator

#### Fields

This function has 1 optional field

1. User ID \(Optional\)

Raw Usage: `$discriminator[userID (optional)]`

#### Options

* User ID - The user we're getting the discriminator from

#### Usage

Getting the author's discrim

```javascript
bot.command({
name: "user", 
code: `$username's is $discriminator`
})
```

Getting the mentioned user's discrim

```javascript
bot.command({
name: "user", 
code: `$username[$mentioned[1]]'s is $discriminator[$mentioned[1]]`
})
```

