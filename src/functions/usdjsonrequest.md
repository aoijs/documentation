---
description: Retrieve a JSON format (api)
---

# $jsonRequest

This function returns a property from a JSON formatted api

```text
$jsonRequest[api;property;error]
```

```javascript
bot.command({
name: "api", 
code: `$jsonRequest[https://some-random-api.ml/facts/dog;fact;Could not fnd a dog fact!]`
})
/*

API Breakdown:
In this api given, if you go to the link it will give you
{"fact":"Putting collars on dogs is an ancient practice, but dog licenses are much more recent."}
So in 'property', you'd put "fact", because it's the only property there to get
Ex:
$jsonRequest[https://some-random-api.ml/facts/dog;fact;Could not fnd a dog fact!]`


But what if the api was like this:
{"dog": {"fact":"Putting collars on dogs is an ancient practice, but dog licenses are much more recent."} }
Then in property, first you'd
need to get "dog", so you'd put 'dog', then to get the fact
add fact after it, like this: 'dog.fact'
Ex:
$jsonRequest[https://some-random-api.ml/facts/dog;dog.fact;Could not fnd a dog fact!]`


But let's say the api has brackets around the thing you
want to get:
{"dog": [{"fact":"Putting collars on dogs is an ancient practice, but dog licenses are much more recent."}] }
So in property, you will still have 'dog' first,
then you'd add brackets as follows: 'dog[0]' 
then simply add on fact. 'dog[0].fact'
WARNING: For DBD.js instead of [] we use #RIGHT# for [ and #LEFT# for ]
Ex:
$jsonRequest[https://some-random-api.ml/facts/dog;dog#RIGHT#0#LEFT#.fact;Could not fnd a dog fact!]`


*/
```

