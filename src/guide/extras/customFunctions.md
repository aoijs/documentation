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

{% hint style="info" %}
WITH THIS FUNCTION MANAGER IT JUST CREATED `$say` FUNCTION
{% endhint %}

## Using the custom function
```javascript
bot.command({
name:"say",
code:`
$say[$authorID;$message]
`
})
```


## Using custom functions for D.js codes:
```javascript
client.functionManager.createCustomFunction({
      name: "$sendDM",//FUNCTION NAME
      type: "djs",//TYPE OF THE FUNCTION
      code: async d => {//FETCHING DATA AS D
        
        const data = d.util.openFunc(d);
        const [userid,message] = data.inside.splits;//GETTING THE PARAMETERS
        
        const user = await d.util.getUser(d, userid);// THIS IS THE CODE INSIDE
        user.send(message);//YOU CAN CHANGE THIS AS PER YOUR REQUIREMENTS
        
        return {
          code: d.util.setCode(data);
        }
        
        
      }
    });
```


{% hint style="danger" %}
ONLY EXPERIENCED WITH UNDERSTANDING OF AOIJS & DISCORD.JS SHOULD USE
{% endhint %}

{% hint style="danger" %}
BY USING CUSTOM FUNCTION WE AREN'T OBLIGED OF WHAT HAPPENS TO YOUR CLIENT
{% endhint %}
