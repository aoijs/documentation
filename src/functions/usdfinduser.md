---
description: 'Find any users, with their username, this is Global.'
---

# $findUser

This function returns the user ID of the given user. Yes/No will determine if function returns current author id \(yes\) or undefined \(no\) if no match was found. Default is yes

#### Fields

This function has 1 required field

1. User \(Required\)
2. Return Current User \(Optional\)

Raw Usage: `$findUser[user;returnCurrentUser (yes/no) (optional)]`

#### Options

* User - The user we're finding
* Return Current User - Whether or not the author's id will be returned if user not found

#### Usage

```javascript
bot.command({
name: "find", 
code: `
$findUser[Kubaturi]`
})
```

