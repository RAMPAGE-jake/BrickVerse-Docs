# Introduction

BrickVerse.co has an official NPMJS Module written in TypeScript by BrickVerse.co, you can use the module by running `npm install brickverse` and requiring it. `require('brickverse');`

## Example

```javascript
const { Client } = requre("brickverse");
let bot = new Client();

bot.login(process.env.BRICKVERSE_SECURITY_TOKEN, false).then(async() => {
    await bot.SendFriendRequest(1);
    
    bot.quit(); // terminates session. this will invalidate your BRICKVERSE SECURITY TOKEN!
})
```
