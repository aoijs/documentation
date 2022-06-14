---
description: Closes a ticket
---

# $closeTicket

This function closes a ticket/channel made by [$newTicket](usdnewticket.md).

### Usage 
```php
$closeTicket[error]
```
### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| error | The error to be returned if channel is not a ticket | number | yes |

## Example

```javascript
bot.command({
name: "close",
code: `$closeTicket[This is not a ticket!]`
})
```

