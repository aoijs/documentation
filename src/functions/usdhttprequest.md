# $httpRequest

This function allows the bot to request a method from/to the given url

### Usage 
```php
$httpRequest[url;method?;body?;property?;error?;headerName:headerValue?...]
```

### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| url | The url you're requesting from/to | url | yes |
| method | The method we're using | alphanumeric | no |
| body | The content | alphanumeric | no |
| property | The property to be retrieved if method is GET. | alphanumeric | no |
| error | The error message if the request failed. | alphanumeric | no |
| header\(s\) | The request headers/values. | alphanumeric | no |

#### Methods

* GET - Request data from a resource
* POST - Send data to a server to create or update a resource

## Examples

- Without optional fields

```javascript
bot.command({
name: 'http',
code: `$httpRequest[https://some-random-api.ml/facts/dog]`
})
```

- With optional fields

```javascript
bot.command({
name: 'http',
code: `$httpRequest[https://some-random-api.ml/facts/dog;GET;;fact;Failed]`
})
```

