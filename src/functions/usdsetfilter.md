---
description: Set filter(s) to playing track(s).
---

# $setFilter

`$setFilter` sets the given filter(s) to track, removes the settled filters.[^1]

  [^1]: *To know other filters as well, please check [FFmpeg filters](https://ffmpeg.org/ffmpeg-filters.html).*

> Requires `@akarui/aoi.music` package.

### Usage 

```php
$setFilter[filters]
```

### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| filters | The filters will be settled to track(s) | string | yes |

## Examples

We already made a "nightcore" filter for you, so there is the example:

```javascript
bot.command({
  name: "filter-nightcore",
  code: `
  $let[filter;$setFilter[{"nightcore": 1.10}]]
  `
//It will make your track like a nightcore, don't use it on a Nightcore Mix :)
});
```

And here it goes for a custom filter from we checked on FFmpeg:

```javascript
bot.command({
  name: "filter-custom",
  code: `
  8D audio: on!
  $let[filter;$setFilter[{"aecho": "1.0:0.8:50:0.5"}]]
  `
//This will make the track like 8D!
});
```

We used `$let` function on there, cause `$setFilter` function returns as a message. `$let` function can be tricky kind of those situtations :)
