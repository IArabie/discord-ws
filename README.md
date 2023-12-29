### Discord WS

> This Project to learning only!

### Usage

```js
const { Client, Constants } = require('./src');
const bot = new Client({ intents: Object.keys(Constants.Intents) })

bot.on('ready', async() => {
    console.log(`${bot.user.username}'s Online!`);
})

bot.on('messageCreate', async(Message) => {
    if(Message.channelId === '') {
        Message.react([
            '✔️',
            '❌'
        ])
    } else if(Message.content.toLowerCase() === 'hi') {
        Message.reply({ content: 'Hi, How are you doing?' });
    } else if(Message.content.toLowerCase() === 'embed') {
        Message.reply({ embeds: [new EmbedBuilder() .setDescription('Hi')] })
    }
})

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