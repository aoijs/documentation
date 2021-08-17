
# $activity
> **This function shows the current activity of the indicated user \(Only if it detects any activity.\), If the indicated user does not have an activity such as a 'custom status' it will show 'none'.**
## Fields
|field|type|description|optional|default value|
|-----|----|-----------|--------|-------------|
|**userId?**|**Snowflake**|id of the user whose activity is to be shown|true|author's id|
## Activities
>* **Custom Status**
>* **Spotify** _\(Listening to\)_
>* **&lt;Game Name&gt**; _\(Playing\)_
>* **Streaming**
## Usage
>```
> $activity | $activity[userId?]
>```
## Example
>```js
>//Without a user ID
>
>bot.command({
>    name: "activity",
>    code: `$activity`
>});
>
>//With a user ID
>
>bot.command({
>    name: "activity",
>    code: `$activity[1234567890]`
>});
>```







