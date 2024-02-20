MatchZy is a plugin for CS2 for running and managing practice/pugs/scrims/matches with easy configuration!

## What can MatchZy do?
MatchZy can solve a lot of match management requirements. It provides basic commands like `!ready`, `!unready`, `!pause`, `!unpause`, `!tac`, `!tech`, etc., matches stats, and much more!

**Feature highlights:**
- Practice Mode with `.bot`, `.spawn`, `.ctspawn`, `.tspawn`, `.nobots`, `.clear`, `.exitprac` and many more commands!
- Warmup with infinite money 🤑
- Knife round (With expected logic, i.e., the team with the most players wins. If the same number of players, then the team with HP advantage wins. If the same HP, the winner is decided randomly)
- Start live match (after side selection is done by knife winner. Knife round can also be disabled by the `.knife` command).
- Automatically starts demo recording and stops recording when the match is ended
- Coaching system - **(Coach need to join team, before `.coach ct` or `.coach t` works)**
- Damage report after every round
- Support for round restore (Currently using the vanilla valve's backup system)
- Provides easy configuration
- And much more!!


## Usage Commands
Most of the commands can also be used using ! prefix instead of . (like !ready or /ready)

- `.ready` Marks the player ready (can also use `.gaben`)
- `.unready` Marks the player unready
- `.pause` Pauses the match in freezetime. (can also use `.p`)
- `.tech` Pauses the match in freezetime.
- `.unpause` Request for unpausing the match. Both teams need to type .unpause to unpause the match
- `.stay` Stays on the same side (For knife winner, after the knife round)
- `.switch` Switches the side (For knife winner, after the knife round)
- `.stop` Restore the backup of the current round (Both teams need to type .stop to restore the current round)
- `.tac` Starts a tactical timeout
- `.coach <side>` Starts coaching the specified side. Example: `.coach t` to start coaching the terrorist side!

### Practice Mode Commands

- `.spawn <number>` Spawns to the provided competitive spawn number of the same team
- `.ctspawn <number>` Spawns to the provided competitive spawn number of CT
- `.tspawn <number>` Spawns to the provided competitive spawn number of T
- `.bot` Adds a bot on the user's current position
- `.nobot` Removes the bot you have spawned (can also use `.kickbot` or `.removebot`)
- `.nobots` Removes all the bots
- `.clear` Clears all the active smokes, molotoves and incendiaries
- `.fastforward` Fastforwards the server time to 20 seconds
- `.god` Turns on god mode
- `.savenade <name> <optional description>` Saves a lineup (can also use `.save <name> <optional description>`)
- `.loadnade <name>` Loads a lineup (can also use `.nade <name>`)
- `.deletenade <name>` Deletes a lineup from the file
- `.importnade <code>` Upon saving a lineup a code will be printed to chat, alternatively those can be retrieved from the savednades.json
- `.listnades <optional filter>` Lists either all saved lineups ever or if given a filter only those that match the filter (can also use `.nades`)
- `.ct, .t, .spec` Switches team to specified team
- `.fas` Forces all other players to the spectator team

### Admin Commands

- `.start` Force starts a match.
- `.restart` Force restarts/resets a match. (**This will stop the match and stop the CSTV recording even if the match is under scrim mode or normally match mode.**) - (can also use `.forcestop`, `.forceend`, `.end` and `.endgame`)
- `.forcepause` Pauses the match as an admin (Players cannot unpause the admin-paused match). (`.fp` for a shorter command)
- `.forceunpause` Force unpauses the match. (`.fup` for shorter command)
- `.restore <round>` Restores the backup of the provided round number.
- `.knife` Toggles the knife round. If disabled, the match will directly go from the Warmup phase to the Live phase.
- `.match` Activates match. This loads in match mode. (**All 10 players need to ready up, for knife-round**)
- `.playout` Toggles playout (If playout is enabled, all rounds would be played irrespective of the winner. Useful in scrims!)
- `.readyrequired <number>` Sets the number of ready players required to start the match. If set to 0, all connected players will have to ready up to start the match.
- `.settings` Displays the current setting, like whether the knife is enabled or not, the value of ready required  players, etc.
- `.map <mapname>` Changes the map
- `.asay <message>` Say as an admin in all chat
- `.reload_admins` Reloads admins from `pXXX.json`
- `.team1 <name>` Sets name for Team 1 (CT by default)
- `.team2 <name>` Sets name for Team 2 (Terrorist by default)
- `.prac` Starts Practice Mode
- `.exitprac` Exits from practice mode and loads Match mode.
- `.rcon <command>` Sends command to the server
