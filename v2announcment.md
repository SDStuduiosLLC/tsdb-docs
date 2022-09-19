# Command Handler v2 Announcement!

## Pre Release Notice
I am (somewhat) working on an overhauled command handler - which (fingers crossed) will FINALLY add slash command support. No promises though. So don't expect any more new features until then.

We do have October 1st scheduled as Milestone 1 (a.k.a - the first public beta release).

?> You can try out the new handler by cloning the "cmdhandlerv2" branch.

Just keep in mind it probably won't be very stable for the next good while.


---


## (Major) Events Timeline
Here you can find major events along the developments of the v2 command handler, along with updates in the Discord server.

### Development Started (0.1.0)
I've really not done much. Just created a new branch, issue and item on project tracker.

### 0.2.1
Added slash command registration via 2 scripts. `syncCommands` automatically imports all commands with `slash: true` added to the command config and `manLoadCommands` adds commands based off what you define with the builders.
**Using either WILL overwrite all existing commands.** Use `manLoadCommands` caution. Deleting slash commands is a royal pain.