---
description: Decodes or Encodes an URL.
---

# $uri

This function decodes or encodes an URL.
> *For full list of encode characters, tap to [here](https://www.w3schools.com/tags/ref_urlencode.ASP).*

### Usage 

```php
$uri[encode/decode;text]
```

### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| encode/decode | The type we will convert to | string | yes |
| text | The text will be converting to | string | yes |

## Examples

* Encoding:

```javascript
bot.command({
  name: "encode",
  code: `
  $uri[encode;Hello Neodevil#0001 !]
  `
// Returns Hello%20Neodevil%230001%20!
})
```

* Decoding

```javascript
bot.command({
  name: "decode",
  code: `
  $uri[decode;Hello%20Neodevil%230001%20!]
  `
// Returns Hello Neodevil#0001 !
});
```
