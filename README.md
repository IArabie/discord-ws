<img src="https://wallpaperaccess.com/full/6632179.png" style="border-radius: 7px; width: 500px">

### Usage

```js
const { Client, Constants } = require('./src');
const bot = new Client({ intents: Object.keys(Constants.Intents) })



bot.login(process.env.DISCORD_TOKEN);

```

```
discord-ws
├── src/
│   └── Client/
│       ├── Client.js
│       ├── WebSocketManager.js
│       └── Events/
│           ├── InteractionCreate.js
│           ├── MessageCreate.js
│           └── ClientReady.js
│ 
├── Classes/
│   ├── Message.js
│   ├── User.js
│   ├── Base.js
│   ├── ClientUser.js
│   ├── MessageReaction.js
│   ├── MessageComponents.js
│   └── Guild.js
│ 
│── Util/
│   ├── BitField.js
│   ├── IntentsBitField.js
│   ├── UserFlagsBitField.js
│   ├── ChannelFlagsBitField.js
│   ├── RoleFlagsBitField.js
│   ├── Utils.js
│   ├── Collection.js
│   ├── Constants.js
│   ├── createEnumerations.js
│   └── Enumerations.js
├── package.json
├── yarn.lock
├── LICENSE
└── .git
```