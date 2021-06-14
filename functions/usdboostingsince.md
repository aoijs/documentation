# $boostingSince

This function will return the amount of time the user has been boosting for. if the user isn't boosting it will return nothing.

#### Fields

This function has 2 optional fields

1. UserID \(Optional\)
2. ms \(Optional\)

Raw usages: `$boostingSince[User ID(Optional);ms (yes/no) (Optional)]`

#### Options

* UserID - The user who we're getting the data from
* ms - Return the time in milliseconds

#### Usage

```javascript
bot.command({
    name: "boosting",
    code: `
    $if[$boostingSince!=]
$username has been boosting since $boostingSince
    $else
You're not boosting!
    $endif
    `
});
```

