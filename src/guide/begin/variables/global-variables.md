---
description: Information that will be saved to all Guilds.
---

# Global Variables

2 Different types of global variables. Normal global variables, then theres global user variables

{% hint style="danger" %}
Make sure, you have the variables added already.
{% endhint %}

## Global Variables

The value will be the same for everyone in every guild

### Setting Variable

```php
$setVar[Variable;Value]
```

### Retrieving Variable

```php
$getVar[Variable]
```

## Global User Variables

The value will be assigned to a user and it will be the same for every guild

### Setting a variable

```php
$setGlobalUserVar[Variable;Value;User ID (optional)]
```

### Retrieving Variable

```php
$getGlobalUserVar[Variable;User ID (Optional)]
```

