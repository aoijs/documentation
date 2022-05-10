---
Description: Show author's banner.
---
<hr>

# $authorBanner

This function will show author's banner, if there's not a banner; it will return **`null`**.

### Usage 
```js
$authorBanner[size?;dynamic?;format?]
```
### Fields
| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| size | Size of the banner | number | no |
| dynamic | Stopping animation (related to animated pictures) | string | no |
| format | Format of the banner (jpg, png etc.) | string | no |

## Example
```js
bot.command({
  name: "author-banner",
  code: `
  Here's your banner!
  
  $authorBanner
  `
});
```
