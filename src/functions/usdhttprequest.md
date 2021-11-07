# $httpRequest

This function allows the bot to request a method from/to the given url

#### Fields

This function has 1 required fields

1. URL \(Required\)
2. Method \(Optional\)
3. Body \(Optional\)
4. Property \(Optional\)
5. Error \(Optional\)
6. Header\(s\) \(Optional\)

Raw Usage: `$httpRequest[url;method (optional);body (optional);property (optional);error (optional);headerName:headerValue;headerName:headerValue (optional);...]`

#### Options

* URL - The url we're requesting from/to
* Method - The method we're using
* Body - The content
* Property - Only if Method is **GET.** 
* Error - The error message if the request failed
* Header\(s\) - The request headers/values

#### Methods

* GET - Request data from a resource
* POST - Send data to a server to create or update a resource

#### Usage

Without optional fields

```javascript
bot.command({
name: 'http',
code: `$httpRequest[https://some-random-api.ml/facts/dog]`
})
```

With optional fields

```javascript
bot.command({
name: 'http',
code: `$httpRequest[https://some-random-api.ml/facts/dog;GET;;fact;Failed]`
})
```

