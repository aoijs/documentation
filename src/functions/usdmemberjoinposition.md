# $memberJoinPosition

This function will show you your position in the joined history. \(1st, 2nd, 3rd member, etc.\)

{% hint style="info" %}
This function requires you to have all server members cached to be accurate.
{% endhint %}

Raw usage: `$memberJoinPosition[User ID (Optional)]`

Example:

```javascript
bot.command({
    name: "joined",
    code: `You are in position: $memberJoinPosition`
});
```

