---
description: How to configure your instance for initial testing and deployment.
---

# Initial Configuration

### Configuring TSAB Instance

Now that we know TSAB installed correctly, it needs to be properly configured. It's pretty easy to do - might just take a bit to get all the keys and tokens you need.

Out of the box, you should be able to find a file called config.example.ts. That's the one you need. Rename it to config.ts. Make sure that Git actually ignores it so you don't accidentally commit ALL of your tokens. I have made that mistake once - and never again!

There are somethings missing from the template below as they are not strictly required for your instance to operate & some preconfigured options, we recommend you keep the defaults - except for the responses, make them unique!

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
      ">>",
    serverId: "",
    logChannel: "",
    staffRole: "",
    /** Array of all bot owners. Set index0 as the main owner/server owner, basically the person you want people to contact when it breaks. */
    botOwners: [""],
    /** Toggle for message commands. Set to false by default for what should be obvious reasons. Read the DDev docs if you want more info on why. */
    messageCommandsEnabled:
      false,
    shardCount: 1, 
  statcord: {
    apiKey: "",
  },
  tsabLoggerSetting: {
    logFilePath: "data/tsab.log", // full path from root of project
    loggingWebhook: "",
  },
}
```
