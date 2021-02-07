# Rust Server Oxide 2x template

A rust server template for Oxide all the main plugins and setup involved for creating a working community driven 2x rust server. This 
template is designed to be dropped over a pre-installed rust oxide server and not a standalone server template. Only plugins/configs are provided.

----------------------------------------------------------------

Run following commands in the server console using an RTC connection.

oxide.grant group admin permissionsmanager.allowed
oxide.grant group admin vanish.use
oxide.grant group admin removertool.admin
oxide.grant group admin admindeepcover.use
oxide.grant group admin godmode.admin
oxide.grant group admin freeze.use

oxide.grant group default skins.use
oxide.grant group default signartist.restore
oxide.grant group default signartist.text
oxide.grant group default signartist.url
oxide.grant group default discordrewards.use
oxide.grant group default furnacesplitter.use

gather.rate dispencer * 2
gather.rate pickup * 2
gather.rate quarry * 2
gather.rate survey * 2

----------------------------------------------------------------

Change following config files to connect to your specific channel ID's and webhooks.

- DiscordChat
- DiscordCore
- DiscordEvents
- DiscordRewards
- DiscordServerStats
- DiscordWipe
- StashTraps
- AutoStashTraps

NOTE: The way they are setup you have to create a new app using discord development and use the API key in DiscordCore.
NOTE: This same API key app will be used for DiscordRewards so the user must message that discord bot with their /verify code to be given the reward.
NOTE: Any other queries or questions for setting up these DiscordConnections to the server can be found by searching the plugin name and following developer guidlines.

See an example of a website and discord server for this sort of rust server setup here:

www.CreepyOutpost.com
https://discord.gg/d2hWyBmPby

Website template:
https://github.com/Lewisscrivens/CreepyOutpostWebsite

There are much better website templates out there by HTML developers for example here:
https://github.com/Mo45/Rust-Server-Website-Template

----------------------------------------------------------------

Change the config for a different welcome message to the server.

LoadingMessages.json   - These are messages shown to a user while loading into the server at random.
ServerInfo.json        - This is the welcome box shown to the user after loading in or after typing /info.

----------------------------------------------------------------

Active server/game commands (Commands with "/" are in-chat based commands)

Skin
- /Skin drop gun into popup box and swap for skin you want.

PhantomSleeper
- createphantom -- Will spawn a phantom player at the position you are looking at. 
- This phantom is automatically given clothing, a weapon, and put to sleep. 
- All items spawned are given random skins to make the sleeper look as unique as possible.

Admin DeepCover
- /deepcover -- become hidden.
- /deepcover <Profile> -- picks specific fake identity using its profile number.

PlayerAdministration
- /padmin -- Show the player administration menu (requires playeradministration.access.show permission)

Permissions panel
- /Perms

Freeze
- /freeze <name or id> -- Freeze the target player
- /unfreeze <name or id> -- Unfreeze the target player
- /freezeall -- Freeze all players currently online
- /unfreezeall -- Unfreeze all players currently online

Godmode
- /god -- Toggle player's godmode on/off; requires godmode.toggle permission
- /god <name or id> -- Toggles target player's godmode on/off; requires godmode.admin permission
- /gods -- List all players with godmode enabled; requires godmode.admin permission

Inventory Viewer
- /viewinventory <name/id>
- /viewinv <name/id>

Admin radar
- /Radar
- /Radar Help

Time
- Console env.time 0 - 20

Hit Icon
- /hit to toggle enable/disable

Teleport
- /tp - Teleports yourself to the target player.
- /tp - Teleports the player to the target player.
- /tp - Teleports you to the set of coordinates.
- /town - Teleports you to town.
- /outpost - Teleports you to outpost.
- /bandit - Teleports you to bandit.

StashTraps
- /stash -- toggles stash placement mode.
- /stash <integer> -- spawns the provided amount of stashes.

AutoStashTraps
- /trap.tele -- teleports you to the last warning location.
- /trap.show -- displays all active stashes on the map.
- trap.generate -- generates new and missing stashes.
- trap.clear -- clears all stashes on the map.
- trap.report -- prints report of active stashes and queued ones to destroy.

Removal
- /remove [time (seconds)] -- Enable/Disable RemoverTool
- /remove <admin | a> [time (seconds)] -- Enable admin RemoverTool. In this mode, any entity can be removed.
- /remove all [time (seconds)] -- Remove everything that touchs each other starting where you are looking at (will remove multiple buildings if they are too close to each other) (might be slow for big buildings)
- /remove <structure | s> [time (seconds)] -- Remove an entire building (won't remove buildings that are close to eachother or deployables) (VERY fast even on big buildings)
- /remove <external | e> [time (seconds)] -- Remove adjacent high external walls
- /remove <help | h> -- View help

Rust Spawner
- /rspawn wolf - Spawns a Wolf
- /rspawn horse - Spawns a Horse
- /rspawn bear - Spawns a Bear
- /rspawn mini - Spawns a Mini Copter
- /rspawn scrapheli - Spawns a Scrap Heli
- /rspawn car - Spawns a Car
- /rspawn zombie - Spawns a Zombie

Sign Artist.
- /sil <url>
- /silt <message> [<fontsize: number>] [<color: hex value>] [<bgcolor: hex value>]
- /silrestore [all]
- /sili

Clans
- /clan create <tag> - Create a new clan
- /clan join <tag> - Join a clan if you have a invite
- /clan leave- Leave you current clan

Clan Moderator Commands
- /clan invite <partialname> - Invite a player to join your clan
- /clan invite cancel <partialname/ID> - Cancel a pending invite
- /clan kick <partialname/ID> - Kick a player from your clan

Clan Owner Commands
- /clan promote <partialname/ID> - Promote a clan member to clan moderator
- /clan demote <partialname/ID> - Demote a clan moderator to clan member
- /clan disband - Disband your clan

Better Chat
- /chat group add <group> -- Creates a new chat group
- /chat group remove <group> -- Removes a chat group
- /chat group set <group> <setting> <value> -- Changes a chat group setting
- /chat group list -- Lists all chat groups
- /chat user add <player|steamid> <group> -- Adds a player to a chat group
- /chat user remove <player|steamid> <group> -- Removes a player from a chat group

Stack Size Controller 
- /stack and /stackall

NOTE: Setup user/group permisions within game using /perms