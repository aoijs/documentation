# $day

This function returns the current day.

#### Usage 
```php
$day[returnDayOfTheWeek?]
```  
### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| returnDayOfTheWeek | Whether to return the day of the week  | yes/no | no|

## Example

```javascript
bot.command({
name: "day",
code: `Day: $day`
})
```

