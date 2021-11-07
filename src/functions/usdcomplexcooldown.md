# $complexCooldown

This function will create a cooldown for one of the 5 times of existing cooldowns.

#### Fields

This function has 2 required fields.

1. Type \(Required\)
2. Time \(Required\)
3. errorMessage \(Optional\)

Raw usage: `$complexCooldown[type;time;errorMessage]`

#### Options

* Type \(user / server / channel / globalUser / all\) - Who will affect this cooldown.
* Time - The cooldown amount of time.
* errorMessage - The error the users should get when they try to run the command without waiting for the cooldown to be up.

#### Usage

```javascript
bot.command({
    name: "uwu",
    code: `uwu
    $complexCooldown[server;15s;Wait %time% more before uwuing again]`
})
```

