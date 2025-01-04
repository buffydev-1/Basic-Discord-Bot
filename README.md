# Discord Basic Bot

This repository contains a simple Discord bot built using Discord.js. The bot can respond to a basic `!ping` command and can be easily extended with additional functionality.

---

## Features
- Responds to the `!ping` command with `Pong!`
- Uses a configurable prefix and bot token via `config.js`

---

## Prerequisites

- [Node.js](https://nodejs.org/) (LTS version recommended)
- A [Discord Developer Portal](https://discord.com/developers/applications) account to create a bot and get a bot token

---

## Setup Instructions

### 1. Clone the Repository
```bash
git clone https://github.com/YOUR_USERNAME/discord-basic-bot.git
cd discord-basic-bot
```

### 2. Install Dependencies
```bash
npm install
```

### 3. Configure the Bot
- Rename `config.example.js` to `config.js`.
- Open `config.js` and replace `YOUR_DISCORD_BOT_TOKEN` with your actual Discord bot token.

```javascript
module.exports = {
  token: 'YOUR_DISCORD_BOT_TOKEN',
  prefix: '!',
};
```

### 4. Run the Bot
```bash
node bot.js
```

You should see a message in the terminal confirming the bot is online:
```
Logged in as BOT_NAME!
```

### 5. Invite the Bot to Your Server
- Go to the [Discord Developer Portal](https://discord.com/developers/applications).
- Select your application, then go to the **OAuth2 > URL Generator** section.
- Select the `bot` scope and grant necessary permissions (e.g., `Send Messages`, `Read Messages`).
- Copy the generated URL and open it in your browser to invite the bot to your server.

---

## Usage
- Type `!ping` in any server channel where the bot is present, and the bot will reply with `Pong!`.

---

## File Structure
```
.
├── index.js         # Main bot logic
├── config.js      # Configuration file (contains token and prefix)
├── package.json   # Project metadata and dependencies
├── README.md      # Documentation
```

---

## Extending the Bot
You can add new commands by extending the `messageCreate` event in `bot.js`. For example:

```javascript
if (command === 'hello') {
  message.reply('Hello, world!');
}
```

---

## License
This project is licensed under the MIT License. See the LICENSE file for details.

---

## Contributing
Contributions are welcome! Feel free to fork this repository and submit a pull request.
