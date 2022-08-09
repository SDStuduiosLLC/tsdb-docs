# Basic Configuration

This is where it could take a while. Make sure you have; 
- A Discord application with bot attached
- A Discord server with;
  - Logging channel
  - At least 1 "Staff" role
- A Twitter developer account
  - You will need to have an app, with API keys and user keys with full permissions
- A MongoDB database

-----

Once you have all of this you can goto the `data/config.ts` file and fill in ALL the fields (unless it says its optional).

This step really isn't that hard.

---

#### Template (config.ts)
```javascript
export const config = {
  responses: {
    // Actually put some time in and customise these, no one wants a generic a** bot ok
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
    token:
      "Your Discord bot token",
    botPrefix: "",
    serverId: "ID of the server the bot is to be linked to",
    logChannel: "ID of the channel (some) logs will be set to",
    staffRole: "ID of the role that STAFF members have",
    adminRole: "ID of the role that ADMIN members have. If you do not have an admin set it to the owner role or create a blank role",
    shardCount: 1, 
    // Make sure to use only a plain number, doing "1" will just crash it. also "auto" doesnt work for some reason
    // This isn't being used but is still required for checks to pass
  },
  twitter: {
    apiKey: "Twitter APP API Key",
    apiSecret: "Twitter APP API Secret",
    bearerToken: "Twitter APP API Bearer",
    // These are USER keys. Not app keys, also the Twitter code is very buggy rn so don't rely on it
    accessKey: "You don't really need these two ATM",
    accessSecret: "",
  },
  mongo: {
    connectionUri:
      "The connection URI to your mongodb database. Make sure all details are filled in and a database name added",
  },
};
```