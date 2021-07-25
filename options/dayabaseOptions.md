# DatabaseOptions 
> ** Available Options Are:**
## db 
### Type
> **"default"** or **module** 
### Description
>```js
> Defines The Database To Be Used
>```
### Usage
>```js
> db:"default" //or db: require('quick.db') (quickdb is taken as example)
>```
---
## path
### Type
> **string** 
### Description
>```js
> Defines The Path Database Will Store The Data //(note:Not all Database Supports Path)
>```
### Usage
>```js
> path:"./database/" // quick.db doesn't support path 
>```
---
## tables 
### Type
> **Array\<string\>**
### Description
>```js
> Creates The Tables 
>```
### Usage
>```js
> tables:["main"]
>```
---
## promisify 
### Type
> **boolean** 
### Description
>```js
> Promisifies A Non Promised Database 
>```
### Usage
>```js
> promisify:false //for "quick.db" , we need to use promisify:true 
>```
---
