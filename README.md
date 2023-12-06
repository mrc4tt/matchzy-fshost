MatchZy is a plugin for CS2 for running and managing practice/pugs/scrims/matches with easy configuration!

## What can MatchZy do?
MatchZy can solve a lot of match management requirements. It provides basic commands like `!ready`, `!unready`, `!pause`, `!unpause`, `!tac`, `!stop`, etc, provides matches stats, and much more!

**Feature highlights:**
- Practice Mode with `.bot`, `.spawn`, `.ctspawn`, `.tspawn`, `.nobots`, `.clear`, `.exitprac` and many more commands!
- Warmup with infinite money 🤑
- Knife round (With expected logic, i.e., team with most players win. If same number of players, then team with HP advantage wins. If same HP, winner is decided randomly)
- Start live match (after side selection is done by knife winner. Knife round can also be disabled).
- Automatically starts demo recording and stop recording when match is ended
- Coaching system - **We can't confirm that it works**
- Damage report after every round
- Support for round restore (Currently using the vanilla valve's backup system)
- Provides easy configuration
- And much more!!


## Usage Commands
Most of the commands can also be used using ! prefix instead of . (like !ready or /ready)

- `.ready` Marks the player ready
- `.unready` Marks the player unready
- `.pause` Pauses the match in freezetime.
- `.tech` Pauses the match in freezetime.
- `.unpause` Request for unpausing the match. Both teams need to type .unpause to unpause the match
- `.stay` Stays on the same side (For knife winner, after the knife round)
- `.switch` Switches the side (For knife winner, after the knife round)
- `.stop` Restore the backup of the current round (Both teams need to type .stop to restore the current round)
- `.tac` Starts a tactical timeout
- `.coach <side>` Starts coaching the specified side. Example: `.coach t` to start coaching terrorist side!

### Practice Mode Commands

- `.spawn <number>` Spawns to the provided competitive spawn number of same team
- `.ctspawn <number>` Spawns to the provided competitive spawn number of CT
- `.tspawn <number>` Spawns to the provided competitive spawn number of T
- `.bot` Adds a bot on user's current position
- `.nobots` Removes all the bots
- `.clear` Clears all the active smokes, molotoves and incendiaries
- `.fastforward` Fastforwards the server time to 20 seconds
- `.god` Turns on god mode
- `.savenade <name> <optional description>` Saves a lineup
- `.loadnade <name>` Loads a lineup
- `.deletenade <name>` Deletes a lineup from file
- `.importnade <code>` Upon saving a lineup a code will be printed to chat, alternatively those can be retrieved from the savednades.json
- `.listnades <optional filter>` Lists either all saved lineups ever or if given a filter only those that match the filter
- `.ct, .t, .spec` Switches team to specified team
- `.fas` Forces all other players to the spectator team

### Admin Commands

- `.start` Force starts a match.
- `.restart` Force restarts/resets a match.
- `.forcepause` Pauses the match as an admin (Players cannot unpause the admin-paused match). (`.fp` for shorter command)
- `.forceunpause` Force unpauses the match. (`.fup` for shorter command)
- `.restore <round>` Restores the backup of provided round number.
- `.knife` Toggles the knife round. If disabled, match will directly go from Warmup phase to Live phase.
- `.playout` Toggles playout (If playout is enabled, all rounds would be played irrespective of the winner. Useful in scrims!)
- `.readyrequired <number>` Sets the number of ready players required to start the match. If set to 0, all connected players will have to ready-up to start the match.
- `.settings` Displays the current setting, like whether knife is enabled or not, value of readyrequired  players, etc.
- `.map <mapname>` Changes the map
- `.asay <message>` Say as an admin in all chat
- `.reload_admins` Reloads admins from `pXXX.json`
- `.team1 <name>` Sets name for Team 1 (CT by default)
- `.team2 <name>` Sets name for Team 2 (Terrorist by default)
- `.prac` Starts Practice Mode
- `.exitprac` Exits from practice mode and loads Match mode.
- `.rcon <command>` Sends command to the server
