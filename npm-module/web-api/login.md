# login

Once you inited a new client you must login into your BrickVerse bot account, simply use Client Object.login(brickverse token)

## Example

```javascript
const { Client } = requre("brickverse");
let bot = new Client();

bot.login(process.env.BRICKVERSE_SECURITY_TOKEN, "player").then(async() => {
    await bot.SendFriendRequest(1);
});
```
