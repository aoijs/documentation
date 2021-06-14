---
description: >-
  Gets the creation date of the specified server, user, channel, message or role
  ID
---

# $creationDate

This function will get the creation date of the specified ID.

#### Fields

This function has 2 fields

1. ID \(Required\)
2. Format \(Optional\)

Raw Usage: `$creationDate[id;format]`

#### Options:

* ID - The ID of the guild, channel, role or user or message
* Format - The format the function will return

#### Format Options:

* `date` =&gt; Exact Date and Time - Example: 11/4/2020, 1:08:06 AM \(default option\)
* `ms` =&gt; Milliseconds of the date - Example: 1604452086625
* `time` =&gt; How long ago - Example: 4 months 2 weeks 4 days 18 hours 32 minutes and 32 seconds

#### Usage:

Using date format of the creation of an user:

```javascript
bot.command({
name: "creationDate",
code: `
Creation Date of Kubaturi: $creationDate[535566311942651924;date]
`
}) 
/*
This will return:
1/17/2019, 9:09:19 PM
*/
```

Using ms format of the creation of an user:

```javascript
bot.command({
name: "creationDate",
code: `
Creation Date of Kubaturi: $creationDate[535566311942651924;ms]
`
}) 
/*
This will return:
1547759359108
*/
```

Using time format of the creation of an user:

```javascript
bot.command({
name: "creationDate",
code: `
Creation Date of Kubaturi: $creationDate[535566311942651924;time]
`
}) 
/*
This will return:
2 years 1 month 3 weeks 3 days 6 hours 42 minutes and 6 seconds
*/
```

