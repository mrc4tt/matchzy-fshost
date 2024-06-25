MatchZy is a plugin for CS2 for running and managing practice/pugs/scrims/matches with easy configuration!
#### This plugin has been modified for FSHOST Pro!

## What can MatchZy do?
MatchZy can solve a lot of match management requirements. It provides basic commands like `!ready`, `!unready`, `!pause`, `!unpause`, `!tac`, `!tech`, etc., matches stats, and much more!

**Feature highlights:**
- Practice Mode many more commands!
- Warmup with infinite money 🤑
- Knife round (With expected logic, i.e., the team with the most players wins. If the same number of players, then the team with HP advantage wins. If the same HP, the winner is decided randomly)
- Start live match (after knife winner makes side selection. Knife round can also be disabled by the `.kniferound <on/off>`, `.kr <on/off>` and `.rk <on/off>` commands).
- Automatically starts demo recording and stops recording when the match is ended
- Coaching system - **(Coach need to join team, before `.coach ct` or `.coach t` works)**
- Damage report after every round
- Support for round restore (Currently using the vanilla valve's backup system)
- Provides easy configuration

## Usage Commands
Most of the commands can also be used using ! prefix instead of . (like !ready or /ready)
- `.ready` Marks the player ready
- `.unready` Marks the player unready
- `.pause` Pauses the match in freezetime (Normal pause).
- `.tech` Pauses the match in freezetime.
- `.unpause` Request for unpausing the match. Both teams need to type **`!unpause`** or **`.unpause`** to unpause the match
- `.stay` Stays on the same side (For knife winner, after the knife round)
- `.switch`/`.swap` Switches the side (For knife winner, after the knife round)
- `.stop` Restore the backup of the current round (Both teams need to type .stop to restore the current round)
- `.tac` Starts a tactical timeout - **You can't unpause this!**
- `.coach <side>` Starts coaching the specified side. Example: `.coach t` to start coaching the terrorist side!

### Practice Mode Commands
- `.spawn <number>` Spawns to the provided competitive spawn number of the same team
- `.ctspawn <number>` Spawns to the provided competitive spawn number of CT
- `.tspawn <number>` Spawns to the provided competitive spawn number of T
- `.bot` Adds a bot on the user's current position
- `.nobot` Removes the bot you have spawned (can also use `.kickbot` or `.removebot` -- This is a custom command, as MatchZy is modified for FSHOST Pro)  
- `.crouchbot` Adds a crouched bot on the user's current position
- `.boost` Adds a bot on the current position and boosts the player on it
- `.crouchboost` Adds a crouched bot on the current position and boosts the player on it
- `.ct`, `.t`, `.spec` Changes player team to the requested team
- `.fas` / `.watchme` Forces all players into spectator except the player who called this command
- `.nobots` Removes all the bots
- `.clear` Clears all the active smokes, molotoves and incendiaries
- `.fastforward` Fastforwards the server time to 20 seconds (can also use: `.ff`)
- `.noflash` Toggles immunity for flashbang (it will still blind others with noflash disabled)
- `.dryrun` Turns on dry-run mode
- `.god` Turns on god mode
- `.savenade <name> <optional description>` Saves a lineup
- `.loadnade <name>` Loads a lineup
- `.deletenade <name>` Deletes a lineup from the file
- `.importnade <code>` Upon saving a lineup a code will be printed to chat, alternatively those can be retrieved from the savednades.cfg
- `.listnades <optional filter>` Lists either all saved lineups ever or if given a filter only those that match the filter
- `.break` Breaks all the breakable entities (glass windows, wooden doors, vents, etc)
- `.rethrow` Rethrows your last thrown grenade
- `.timer` Starts a timer immediately and stops it when you type .timer again, telling you the duration of time
- `.last` Teleports you back to where you threw your last grenade from
- `.back <number>` Teleports you back to the provided position in your grenade history
- `.delay <delay_in_seconds>` Sets a delay on your last grenade. This is only used when using .rethrow or .throwindex
- `.throwindex <index> <optional index> <optional index>` Throws grenade of provided position(s) from your grenade thrown history. Example: `.throwindex 1 2` will throw your 1st and 2nd grenade. `.throwindex 4 5 8 9` will throw your 4th, 5th, 8th and 9th grenade (If you've added delay in grenades, they'll be thrown with their specific delay).
- `.lastindex` Prints the index number of your last thrown grenade.
- `.rethrowsmoke` Throws your last thrown smoke grenade.
- `.rethrownade` Throws your last thrown HE grenade.
- `.rethrowflash` Throws your last thrown flash.
- `.rethrowmolotov` Throws your last thrown molotov.
- `.rethrowdecoy` Throws your last thrown decoy.
- `.previewnade` / `.nadecam` This toggle enables or disables a picture-in-picture preview showing the trajectory of grenades in practice mode. (**sv_grenade_trajectory_prac_pipreview**)

### Admin Commands
- `.start` Force starts a match.
- `.restart` Force restarts/resets a match. (**This will stop the match and stop the CSTV recording even if the match is under scrim mode or normally match mode.**)
- `.forcepause` Pauses the match as an admin (Players cannot unpause the admin-paused match). (`.fp` for a shorter command)
- `.forceunpause` Force unpauses the match. (`.fup` for shorter command)
- `.restore <round>` Restores the backup of the provided round number.
- `.rk <on/off>` Toggles the knife round. If disabled, the match will directly go from the Warmup phase to the Live phase. (Can also use: `.kr <on/off>`, `.kniferound <on/off>`)
- `.match` Activates match. This loads in match mode. (**All 10 players need to ready up, for knife-round**)
- `.scrim` Activates scrim. This loads in scrim mode. (**All 10 players need to ready up, NO KNIFE ROUND!** - All rounds would be played irrespective of the winner. Useful in scrims!)
- `.readyrequired <number>` Sets the number of ready players required to start the match. All connected players will have to be ready to start the game.
- `.settings` Displays the current setting, like whether the knife is enabled or not, the value of ready required players, etc.
- `.team1 <name>` Sets name for Team 1 (CT by default)
- `.team2 <name>` Sets name for Team 2 (Terrorist by default)
- `.prac` Starts Practice Mode
- `.exitprac` Exits from practice mode and loads Match mode.
- `.rcon <command>` Sends command to the server
