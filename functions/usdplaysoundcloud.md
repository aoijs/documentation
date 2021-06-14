# $playSoundCloud

This function plays music from sound cloud

This function has 6 fields:

1. URL \(Required\)
2. Soundcloud client ID \(Optional\)
3. Time before leaving vc \(When queue empty\) \(Optional\)
4. Deaf \(yes/no\) \(Optional\)
5. Leave when vc empty \(yes/no\) \(Optional\)
6. Error \(Optional\)

Raw usage: `$playSoundCloud[url;soundcloud client id (optional);leave vc time;defean (yes or no);leave when vc empty (yes/no);error]`

Example:

```javascript
bot.command({
name: "playSoundcloud",
code: `$playSoundCloud[https://soundcloud.com/aviciiofficial/the-nights;client_id;1m;yes;yes;:x: An error has ocurred]`
})
```

## Client ID

![](../.gitbook/assets/image%20%2845%29.png)

A full guide can be found here : [https://github.com/zackradisic/node-soundcloud-downloader\#client-id](https://github.com/zackradisic/node-soundcloud-downloader#client-id)

