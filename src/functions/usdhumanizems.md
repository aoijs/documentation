# $humanizeMS

This function converts MS time into a readable duration

#### Fields

This function has 1 required field

1. MS \(Required\)
2. Limit \(Optional\)
3. Separator \(Optional\)

Raw Usage: `$humanizeMS[ms;limit (optional);separator (optional)]`

#### Options

* MS - The duration in ms we're converting
* Limit - Limit of display for the duration
* Separator - The separator for each duration

#### Usage

Without the optional fields

```javascript
bot.command({
name: "convert",
code: `
$humanizeMS[1207398129310]
`
//Returns: 38 years and 9 months
})
```

With `Limit` optional field

```javascript
bot.command({
name: "convert",
code: `
$humanizeMS[1207398129310;4]
`
//Returns: 38 years 9 months 24 days and 12 hours
})
```

With `Separator` optional field

```javascript
bot.command({
name: "convert",
code: `
$humanizeMS[1207398129310;4;,]
`
//Returns: 38 years, 9 months, 24 days, and 12 hours
})
```

