---
description: Sets an user into timeout.
---

# $timeoutMember

This function sets an user into timout for a set time period

{% hint style="danger" %}
Your client must have MODERATE_MEMBERS permission to use this function
{% endhint %}

#### Fields

This function has 2 required fields

1. userID \(Required\)
2. time \(Required\) 

Raw Usage: `$timeoutMember[userID (required);time (60s or 5m or 10m or 1h 1d or 1w)(required);reason (optional)]`

#### Options

* Reason - The reason why the user is getting timed out


#### Usage

Without a reason

```javascript
bot.command({
    name: "timeout",
    code: `$timeoutMember[$mentioned[1];60s;]`
});
```

With a reason

```javascript
bot.command({
    name: "timeout",
    code: `$timeoutMember[$mentioned[1];5m;wasn't being nice >:( ]`
});
```
