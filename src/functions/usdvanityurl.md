---
description: Returns vanity URL.
---

# $vanityURL

This function returns the current servers vanity URL, if they have one.

> * What's Vanity URL?
> A custom URL Redirects you to a server. This would be a vanity URL `discord.gg/akarui`. For example, this is not a vanity URL `https://discord.com/invite/j352EV9ran`


### Usage

```php
$vanityURL
```

## Example

```javascript
bot.command({
  name: "vanity-url",
  code: `
  URL: $vanityURL
  `
});
```
