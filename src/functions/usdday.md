# $day

This function returns the current day.

#### Fields

This function has 1 optional field

1. Return Day of the Week \(Optional\)

Raw usage: `$day[returnDayOfTheWeek (yes/no) (optional)]`  

#### Options

* Return Day of the Week - Whether or not it returns the specified day - Example: Monday

#### Usage

```javascript
bot.command({
name: "day",
code: `Day: $day`
})
```

