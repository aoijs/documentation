# $hoistedRole

This function returns the highest hoisted role's ID the given user has

### Usage 
```php
$hoistedRole[userID?;guildID?;option?]
```

### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
|user ID|The id of the user whose role is to be returned|number|no|
| guild ID | The id of the guild | number | no |
| option | The option on basis of which the role will be returned | string | no |

#### Options
- `id` - Returns id of the role.
- `name` - Returns name of the role.
- `mention` - Returns the mention of the role.

## Example

- Without optional fields

```javascript
bot.command({
name: 'hoistedRole',
code: `$hoistedRole`
})
```

- With optional fields

```javascript
bot.command({
name: 'hoistedRole',
code: `$hoistedRole[$mentioned[1];$guildID;mention]`
})
```

