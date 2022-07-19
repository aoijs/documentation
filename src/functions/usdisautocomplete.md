---
description: Returns boolean of slash choice.
---

# $isAutoComplete

`$isAutoComplete` is used to checking the if interaction command's *interaction autocomplete* feature enabled or disabled.

### Usage

```php
$isAutoComplete
```

## Example

```javascript
module.exports = {
  name: "is-auto-complete",
  type: 'interaction',
  prototype: 'slash',
  code: `
  $interactionReply[
    $if[$isAutoComplete==true;It's enabled.; No, it is not enabled.]
  ]
  `
}
