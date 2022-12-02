# Installing & Configuring

### Cloning & Installing

To get started, clone the main branch from GitHub.

```bash
git clone https://github.com/sd-studios-official/the-somewhat-awesome-bot.git
```

After the repository has been successfully cloned, first make sure you have the required **global** dependencies installed. The command for installing them is:&#x20;

```bash
npm install --global typescript ts-node @types/node nodemon
```

Once all of these have been successfully installed, just run the NPM install command and wait for it to complete installing packages.

### Checkpoint 1

Now, before continuing - it's best just to check that everything installed correctly. Before running, we need to compile everything back into JavaScript. Run the build command shown below:

```bash
npm run build
```

If all is correctly installed, you should get the following output in the console.

```
if (!key) throw new Error('"key" is missing or undefined');
                        ^
Error: "key" is missing or undefined
```

or

```
No server specified, exit to prevent further errors...
```

If you get this, it worked! Everything has successfully installed.

### Configuring TSAB Instance

Now that we know TSAB installed correctly, it needs to be properly configured. It's pretty easy to do - might just take a bit to get all the keys and tokens you need.

Out of the box, you should be able to find a file called config.example.ts. That's the one you need. Rename it to config.ts. Make sure that Git actually ingores it so you don't accidentally commit ALL of your tokens. I have made that mistake once - and never again!

Here's a copy of the config template if you need/want it for some reason.

```typescript
export const config = {
  responses: {
    noPermission: "You do not have permission to use this command.",
    genericError:
      "Something went wrong. Hopefully the developer adds in extra info!",
    botMissingPermissionSEND_MESSAGES:
      "Missing Permissions! Please grant the bot the `SEND_MESSAGES` permission or reinvite the bot with the correct permissions.",
    botMissingPermissionEMBED_LINKS:
      "Missing Permissions! Please grant the bot the `EMBED_LINKS` permission or reinvite the bot with the correct permissions",
    botHasAdmin:
      "Woah! The server admins are treading a dangerous road, I have admin! If my token gets leaked I could cause havoc! Please ask server admins to remove my administrator permissions.\n\nI will also send a message to the log channel if there is one available.",
  },
  discord: {
    token: "",
    clientId: "",
    /** String of the prefix used to trigger the bot. Pinging the bot is a WIP at the moment. */
    botPrefix:
      "",
    serverId: "",
    logChannel: "",
    staffRole: "",
    /** Array of all bot owners. Set index0 as the main owner/server owner, basically the person you want people to contact when it breaks. */
    botOwners: [""],
    /** Toggle for message commands. Set to false by default for what should be obvious reasons. Read the DDev docs if you want more info on why. */
    messageCommandsEnabled:
      false,
    shardCount: 1, 
  mongo: {
    connectionUri: "",
  },
  statcord: {
    apiKey: "",
  },
  tsabLoggerSetting: {
    logFilePath: "", // full path from root of project
    loggingWebhook: "",
  },
}
```
