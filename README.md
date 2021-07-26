# Aoijs
> **Welcome To The Home Page Of Aoi.js Documentation**
# Introduction
## Logo
![](https://aoi.js.org/assets/images/aoijs-new.png)
## Stats 
[![Discord Server](https://img.shields.io/discord/773352845738115102?color=5865F2&logo=discord&logoColor=white)](https://aoi.js.org/invite) [![NPM Version](https://img.shields.io/npm/v/aoi.js.svg?maxAge=3600)](https://www.npmjs.com/package/aoi.js) [![NPM Downloads](https://img.shields.io/npm/dt/aoi.js.svg?maxAge=3600)](https://www.npmjs.com/package/aoi.js)
## Quick About 
> ___Aoi.JS is a package with simplified and ready-to-use functions for Discord Bot Developers to develop their own Discord Bots.___
>
> ___Aiming to be the easiest package to learn___
> ___It's swift and flexible using functions.___
>
> ___Open Source for the Community ❤️___
# Installation 
> ```js
> "npm i aoi.js"
>```

> **Note:** 
>```js
> NodeJs Version 14 And Above Is Required.
>```
# Basic Examples 
>```js
> const Aoijs = require('aoi.js')
> const bot = new Aoijs.Bot({
> token:"Your Bot Token",
> prefix:"Bot Prefix",
> intents:"all"
> })
>
>bot.onMessage() //enables bot to see messages (required for executing Commands)
>
>bot.command({
>name:"ping", //command name
>code:`My Ping Is \`$ping ms\` ` //code to be executed when this command is called 
>})
>
>```
# Quick Links
## Documentation  
> * **[Classes](class/readme.md)**
> * **[Callbacks](callbacks/readme.md)**
> * **[Functions](functions/readme.md)**
> * **[Guides](guide/readme.md)**
## GitHub
> * **[Aoijs](https://github.com/aoijs/aoi.js)**
> * **[Documentation](https://github.com/aoijs/documentation)**
## Contribution 
> * **[Contribution GuideLines](https://github.com/aoijs/aoi.js/blob/master/.github/CONTRIBUTING.md)**
## Misc
> * **[Discord Server Invite Link 1](https://discord.gg/akarui)**
> * **[Discord Server Invite Link 2](https://discord.gg/3PyVg9U6Xh)**
> * **[Website](https://aoi.js.org)**
