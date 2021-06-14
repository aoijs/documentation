# $formatDate

This function formats a specified time to the given format

#### Fields

This function has 1 required field

1. Time \(Required\)
2. Format \(Optional\)

Raw Usage: `$formatDate[time;format (Optional)]`

#### Options

* Time - The time to be formatted
* Format - The format on how you want the date to be returned

#### Time Options

* datestamp - Example: 1615571386000
* milliseconds - Example: 31556926000ms
* stringed date - Example: 1/17/2019, 9:09:19 PM
* ISO String - Example: 2021-3-12T14:48:00.000Z

#### Format Options

* Blank \(No format provided\) - Example: Friday, 12 March 2021
* LT - Time - Example: 4:01 AM
* LTS - Time w/ seconds - Example: 3:58:5 AM
* L - Date - Example: 3/12/2021
* LLL - Specified Date - Example: March 12 2021 4:02 AM
* LLLL - - Specified Date w/ Day - Example: Friday, March 12 2021 4:02 AM
* dddd - Day - Example: Friday
* HH - Hour - Example: 15
* For more formats, check [here](https://thecodebarbarian.com/formatting-javascript-dates-with-moment-js.html)

#### Usage

Simple Usage

```javascript
bot.command({
name: "formatDate",
code: `
$formatDate[$dateStamp]
`
/*
Returns: 
Friday, 12 March 2021
*/
})
```

Usage w/ format options

```javascript
bot.command({
name: "formatDate",
code: `
$formatDate[$dateStamp;LLLL]
`
/*
Returns: 
Friday, March 12 2021 1:00 PM
*/
})
```

Usage w/ format options & custom text

```javascript
bot.command({
name: "formatDate",
code: `
$formatDate[$dateStamp;dddd at Hour HH]
`
/*
Returns: 
Friday at Hour 13
*/
})
```

