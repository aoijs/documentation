---
description: 'Discord API Intents, these are needed to access certain functionalities of Discord's API.'
---

# Gateway Intents

Gateways are Discord's form of real-time communication over secure WebSockets. Clients will receive events and data over the gateway they are connected to and send data over the REST API.  
  
This will be needed for us to interact with the Discord API and the functions that are prepared to build your bot.  
  
You can enable this in the [Discord Developer Portal through your Bot Application](https://discord.com/developers/applications).

![Discord Gateway Intents](../../.gitbook/assets/screenshot_820.png)

And there we go, You're now able to access their API and you shouldn't have any errors (_besides the errors in your own code_).

If your bot is verified and you don't have the intents enabled, and you want to enable them,  you will need to [Submit a request](https://support.discord.com/hc/en-us/requests/new?ticket_form_id=360005592534). Then, explain what intents you want to use in and why.
