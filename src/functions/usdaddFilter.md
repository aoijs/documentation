---
Description: Adds filter(s) to playing track(s).
---
<hr>

# $addFilter

`$addFilter` adds the given filter(s) to track, removes the settled filters.

> Requires `@akarui/aoi.music` package.

### Usage 
```js
$addFilter[filters]
```
### Fields
| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| filters | The filters will be added to track | string | yes |

###### Footnotes
* *To know other filters as well, please check [FFmpeg filters](https://ffmpeg.org/ffmpeg-filters.html).*

## Examples
We already made a "nightcore" filter for you, so there is the example:
```js
bot.command({
  name: "filter-nightcore",
  code: `
  $let[filter;$addFilter[{"nightcore": 1.10}]]
  `
//It will make your track like a nightcore, don't use it on a Nightcore Mix :)
});
```
And here it goes for a custom filter from we checked on FFmpeg:
```js
bot.command({
  name: "filter-custom",
  code: `
  $let[filter;$addFilter[{"aecho": "1.0:0.8:5:0.5"}]]
  `
//This will make the track like 8D!
});
```
We used `$let` function on there, cause `$addFilter` function returns as a message. `$let` function can be tricky kind of those situtations :)
