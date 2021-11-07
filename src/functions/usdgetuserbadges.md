---
description: 'Retrieves, the Badges, from the User ID.'
---

# $getUserBadges

This function returns the badges a user has. It can only retrieve house and developer badges. Nitro Badges aren't possible

```javascript
$getUserBadges[userID]
```

```javascript
bot.command({
name: "badges", 
code: `$getUserBadges[608358453580136499]`
/*
Would return:
House Balance, Early Verified Developer, Verified Developer
*/
})
```

