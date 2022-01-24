[![Fire Extinguisher Downloads](http://cf.way2muchnoise.eu/full_567798_downloads.svg)](https://www.curseforge.com/minecraft/mc-mods/lobby)
[![Fire Extinguisher MC Versions](http://cf.way2muchnoise.eu/versions/Minecraft_567798_all.svg)](https://www.curseforge.com/minecraft/mc-mods/lobby)

# Lobby and Mining Dimension

Provides a easy to use lobby and optimized mining dimension for you and your friends.

## Features ⭐

- Easy to use, no extra setup needed.
- Optimized mining dimension without mobs and without additional items.
- Provides /lobby, /mining and /spawn commands for the players.
- Changed automatically the user game mode depending on the dimension.
- Customization over the config file and data files, if needed.
- Default lobby will be automatically expand with additional features.

## Lobby Dimension

The lobby dimension is a place to hang out with friends or to enjoy some of the provided content (wip).
But you are free to build your own lobby as well or you can just expand the existing lobby.

All players are automatically in the adventure game mode in the lobby.

![Screenshot of the lobby dimension][lobby_dimension]

## Mining Dimension

The mining dimension will be generated on the first load over the `/mining` command.
It will not include any treasure chest or any mobs, so it could be only use for mining.
You will start in a mining base which provides you some of the basic stuff.
To return to the mining base just use the `/mining` command.

![Screenshot of the mining dimension][mining_dimension]

## User Commands

- **/lobby** teleports you to the lobby
- **/mining** teleports you to the mining dimension
- **/spawn** teleports you to the overworld

## Customization

You can customize the lobby and mining dimension over data files or by changing to creative mode.

**Please make sure to create regular backups for your lobby and/or customized mining dimension.**

### Lobby Customization

The lobby will be automatically in the game mode adventure.
Use the following data files to customize the lobby:

- data/lobby/dimension/lobby_dimension.json
- data/lobby/dimension_type/lobby_dimension.json
- data/lobby/functions/lobby_dimension_load.mcfunction
- data/worldgen/biome/biome_lobby.json

**Note:** The `lobby_dimension_load.mcfunction` file will be only loaded once (per world) to make sure your changes are not overwritten.

### Mining Customization

The optimization are parts of the code, you can use the following data files for customization:

- data/lobby/dimension/mining_dimension.json
- data/lobby/dimension_type/mining_dimension.json
- data/lobby/functions/mining_dimension_load.mcfunction

**Note:** The `mining_dimension_load.mcfunction` file will be only loaded once (per world) to make sure your changes are not overwritten.

[mining_dimension]: https://raw.githubusercontent.com/MarkusBordihn/BOs-Lobby/main/examples/mining_dimension.png
[lobby_dimension]: https://raw.githubusercontent.com/MarkusBordihn/BOs-Lobby/main/examples/lobby_dimension.png
