# $queue

This function returns the queue of songs

```text
$queue or $queue[page;amount;{number} - {title} by <@{userID}>]
```

Available Options:
* {number} - Position in queue
* {userID} - User who added song
* {title} - Title of song
* {url} - Song url
* {description} - Song description
* {duration} - Duration of song
* {publisher} - Publisher of song
* {publisher_url} - Song publisher url
* {username} - Song requester username
* {discriminator} - Song requester discriminator
* {usertag} - Song requester user tag

```javascript
bot.command({
name: "queue",
code: `$queue[1;10;{number} - {title} by <@{userID}>]`
})
```

