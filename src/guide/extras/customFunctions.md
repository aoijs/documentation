# Custom Functions
## Creating the custom function
```javascript
bot.functionManager.createCustomFunction({
name : '$say', //FUNCTION NAME 
params : ['authorid','message'],//THE TYPE OF PARAMS
type : 'aoi.js', //TYPE METHOD
code : ` 
**$userTag[{authorid}]** says: **{message}**
` //THE ACTUAL CODE IT WILL BE RETURN
})
```
## Using the custom function
```javascript
bot.command({
name:"say",
code:`
$say[$authorID;$message]
`
})
```
{% hint style="info" %}
WITH THIS FUNCTION MANAGER IT JUST CREATED `$say` FUNCTION
{% endhint %}

{% hint style="danger" %}
ONLY EXPERIENCED WITH UNDERSTANDING OF AOIJS SHOULD USE
{% endhint %}

{% hint style="danger" %}
BY USING CUSTOM FUNCTION WE ARE'T OBLIGED OF WHAT HAPPENS TO YOUR CLIENT
{% endhint %}
