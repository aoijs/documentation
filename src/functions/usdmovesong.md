# $moveSong

This function moves a song from x to y. If `y` is an invalid position, it will remove the song from the queue

```text
$moveSong[from;to]
```

First thing we should recognize our queue. Lets make up a queue to use for moveSong

1. Marshmello ft. Bastille - Happier \(Official Music Video\)
2. Lukas Graham - 7 Years \[Official Music Video\]
3. Gotye - Somebody That I Used To Know \(feat. Kimbra\) - official music video

```javascript
bot.command({
name: "moveSong",
code: `
$moveSong[2;3]
`
/*
Using our example queue, our code just moved
the second song in queue (Lukas Graham - 7 Years [Official Music Video])
to the third song in queue

So our new queue will look like:
1. Marshmello ft. Bastille - Happier (Official Music Video)
2. Gotye - Somebody That I Used To Know (feat. Kimbra) - official music video
3. Lukas Graham - 7 Years [Official Music Video]
*/
})
```

