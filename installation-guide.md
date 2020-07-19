---
description: These are the steps to follow to get the bot working.
---

# Installation Guide

{% hint style="info" %}
Owning a VPS is highly recommended. Although you can use sites such as repl.it, they do not grant a full uptime and speed. However, you will find a guide to host the bot if you do not have a VPS in this documentation.
{% endhint %}

{% hint style="warning" %}
Make sure you have [Node](https://nodejs.org/en/) installed. 
{% endhint %}

### Creating a Discord App

1. Go to [Discord's Developer Portal](https://discord.com/developers/applications).
2. Create an application and make a bot from it.
3. Copy your token into a safe place.

### Setting Up the Bot

1. Go to the [GitHub Repository](https://github.com/ThePhoDit/ModMail) and fork it.
2. Clone the forked repository.
3. Get into de new created folder.
4. Run `npm run setup` in your CLI.
5. Create a file named `.env` and add your Bot's token in there as shown.

```text
BOT_TOKEN=YOUT_TOKEN_GOES_HERE
```

### Configuring Variables

Open the file `src/config.ts`. You will see some fields you need to fill in.

| Field | Description | Required |
| :--- | :--- | :--- |
| bot\_prefix | The prefix commands will work with. | True |
| bot\_status | The status your bot will display. | False |
| bot\_category | The category ID where new threads will be opened. | True |
| bot\_managers | Array of role IDs that will be able to interact with commands that require having MANAGER permissions. | False |
| bot\_helpers | Array of role IDs that will be able to interact with commands that require having HELPER permissions. | False |
| logs\_channel | Channel ID where logs will be sent. | False |
| role\_ping | Role ID that will be pinged on thread creation. | False |
| messages | Messages that the bot sends. Everyone is self-explained. | False |

### Starting the Bot

{% hint style="info" %}
Using a node runtime such as PM2 is recommended.
{% endhint %}

#### Using PM2

```bash
npm run build && pm2 start prod/index.js --name modmail
```

#### Starting the Bot without PM2

```bash
npm run start
```

