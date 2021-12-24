---
description: Sets an user into timeout.
---

# $addTimeout

This function sets an user into timout for a set time period

#### Fields

This function has 2 required fields

1. userID \(Required\)
2. time \(Required\) 

Raw Usage: `$addtimeout[userID (required);time (60s or 5m or 10m or 1h 1d or 1w)(required);reason (optional)]`

#### Options

* Reason - The reason why the user is getting timed out


#### Usage

Without a reason

```javascript
bot.command({
    name: "timeout",
    code: `$timeout[$mentioned[1];60s;]`
});
```

With a reason

```javascript
bot.command({
    name: "timeout",
    code: `$timeout[$mentioned[1];5m;wasn't being nice >:( ]`
});
```
