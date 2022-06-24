# Custom Functions

Custom functions are used to create special functions with custom code that can only be used by the specific client.

### Usage
```javascript
bot.functionManager.createCustomFunction({
name : '$name', //FUNCTION NAME 
params : ['params',...],//THE TYPE OF PARAMS. Use {param} to get the values of the parameters.
type : 'aoi.js/djs', //TYPE METHOD
code : `The code to be returned` //THE ACTUAL CODE IT WILL BE RETURN
})
```

### Fields
| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| name | The name of the custom function | string with $ sign | yes |
| params | The parameters of the function | string | no |
| type | The type of function to be used | aoi.js or djs | yes |
| code | The code to be returned | alphanumeric | yes |

{% hint style="info" %} To get the values of the parameters provided in the function, use {} around the parameter name i.e. {param}  {% endhint %}

## Examples

### Example with aoi.js function

- Creating the custom function

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

- Using the custom function

```javascript
bot.command({
name:"say",
code:`
$say[$authorID;$message]
`})
```


### Example with discord.js function

- Creating the custom function

```javascript
client.functionManager.createCustomFunction({
      name: "$sendDMtoUser",//FUNCTION NAME
      type: "djs",//TYPE OF THE FUNCTION
      code: async d => {//FETCHING DATA AS D
        
        const data = d.util.openFunc(d);
        const [userid,message] = data.inside.splits;//GETTING THE PARAMETERS
        
        const user = await d.util.getUser(d, userid);// THIS IS THE CODE INSIDE
        user.send(message);//YOU CAN CHANGE THIS AS PER YOUR REQUIREMENTS
        
        return {
          code: d.util.setCode(data);
        }}
    });
```

- Using the custom function

```javascript
bot.command({
name:"dm",
code:`
$sendDMtoUser[$authorID;$message]
`})
```

{% hint style="info" %} You can create a function without parameters by omitting the params field as it is optional. {% endhint %}

{% hint style="danger" %} Only Experienced Developers with proper understanding of aoi.js should use this! {% endhint %}

{% hint style="danger" %} By using custom function we aren't obliged of what happens to your client! {% endhint %}
