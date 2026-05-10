### **Placeholders**

This plugin supports software such as [PlaceholderAPI](https://placeholderapi.com/)

A placeholder is a string such as `%hs_team%`, which in this case returns what team you are on

#### Game Information

The following placeholders can be used to get information about the current state of the game lobby:
- `%hs_status%` - Returns the current status of the game (Waiting, Starting, In-game, Ending).
- `%hs_players%` - Returns the total number of players currently in the lobby/game.
- `%hs_minplayers%` - Returns the minimum number of players required to start the countdown.
- `%hs_maxplayers%` - Returns the maximum number of players allowed in the lobby.
- `%hs_map%` - Returns the name of the current map.

#### Teams

The following teams: `hiders`, `seekers`, and `spectators` can be used in `%hs_<team>%` to get
the number of players currently in that team.

Also `%hs_team%` returns your current team.

#### Rankings

The valid player statistics are:
- `wins`, `hiderWins`, `seekerWins`
- `losses`, `hiderLosses`, `seekerLosses`
- `games`, `hiderGames`, `seekerGames`
- `kills`, `hiderKills`, `seekerKills`
- `deaths`, `hiderDeaths`, `seekerDeaths`

**To get the RANK of a statistic for a target use:**

`%hs_rank_<stat>_<target>`

- When target is not set, it returns the subject players integer rank
- When target is a player name/uuid, it returns the targets integer rank
- When target is an integer rank, it returns the player name at that rank

**Examples:**
- %hs_rank_wins%
- %hs_rank_deaths_KenshinEto$
- %hs_rank_games_1%

#### Stats

**To get the VALUE of a statistic for a target use:**

`%hs_stat_<stat>_<target>`

- When target is not set, it returns the subject players stat value
- When target is a player name/uuid, it returns the stat value for that player
- When target is an integer rank, it returns the stat value at that ranking place (1st/2nd/3rd/...)

**Examples:**
- %hs_stat_wins%
- %hs_stat_deaths_KenshinEto$
- %hs_stat_games_1%
