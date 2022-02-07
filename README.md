[![Lobby, Fishing and Mining Dimension Downloads](http://cf.way2muchnoise.eu/full_567798_downloads.svg)](https://www.curseforge.com/minecraft/mc-mods/lobby)
[![Lobby, Fishing and Mining Dimension Versions](http://cf.way2muchnoise.eu/versions/Minecraft_567798_all.svg)](https://www.curseforge.com/minecraft/mc-mods/lobby)

# 🏝 Lobby, Fishing and Mining Dimension

Provides a easy to use lobby, fishing and optimized mining dimension for you and your friends.

## Features ⭐

- Easy to use, no extra setup needed.
- Optimized mining dimension (configurable: without spawner, mobs, bats or minecart chest).
- Provides /lobby, /mining, /fishing and /spawn commands for the players.
- Changed automatically the user game mode depending on the dimension.
- Customization over the config file and data files, if needed.
- Default lobby will be automatically expand with additional features.
- Automatically transfer users to the lobby on first join or after server restart.

**Note: Please make sure to create regular backups of your dimensions, before installing or updating this mod.**

## Lobby Dimension

The lobby dimension is a place to hang out with friends or to enjoy some of the provided content (wip).
But you are free to build your own lobby as well or you can just expand the existing lobby.

All players are automatically in the adventure game mode in the lobby.

![Screenshot of the lobby dimension][lobby_dimension]

## Mining Dimension

The mining dimension will be generated on the first load over the `/mining` command.
It will not include any treasure chest or any mobs, so it could be only use for mining.
(This could be changed over the config file, if needed.)

You will start in a mining base which provides you some of the basic stuff.
To return to the mining base just use the `/mining` command.

![Screenshot of the mining dimension][mining_dimension]

**Note:** The first load of the dimension could take some time, because the need to generate the world and preparing the spawning area.

## Fishing Dimension

The fishing dimension will be generated on the first load over the `/fishing` command.
It will include only fish's and ocean relevant structures.
All players are automatically in the adventure game mode in the fishing dimension.

![Screenshot of the fishing dimension][fishing_dimension]

## User Commands

- **/fishing** teleports you to the fishing dimension
- **/lobby** teleports you to the lobby
- **/mining** teleports you to the mining dimension
- **/spawn** teleports you to the overworld

## Customization

You can customize the fishing, lobby and mining dimension over data files or by changing to creative mode.

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

### Fishing Customization

The fishing dimension will be automatically in the game mode adventure.
Use the following data files to customize the lobby:

- data/lobby/dimension/fishing_dimension.json
- data/lobby/dimension_type/fishing_dimension.json
- data/lobby/functions/fishing_dimension_load.mcfunction
- data/worldgen/biome/biome_fishing.json

**Note:** The `fishing_dimension_load.mcfunction` file will be only loaded once (per world) to make sure your changes are not overwritten.

## FAQ

### How can I reset a dimension ?

Just delete the dimension and the starting bases will be automatically regenerated after the server restart.

Relevant folders:

- dimensions/lobby/fishing_dimension
- dimensions/lobby/lobby_dimension
- dimensions/lobby/mining_dimension

### How can I reset the default bases like the mining base, fishing base or the spawn without resetting the dimension ?

Teleport to the corresponding dimension and run the corresponding functions like:

- `/function lobby:fishing_dimension_load`
- `/function lobby:lobby_dimension_load`
- `/function lobby:mining_dimension_load`

**Note: This will overwrite any existing block, but no entities see <https://bugs.mojang.com/browse/MC-102430>.**

### How can I remove all entities from the mining dimension from other Mods ?

Just use the following admin command: `/execute in lobby:mining_dimension run kill @e[type=!player,distance=0..]`

### The users are not instantly transferred to the lobby dimension on their first join. Any way to fix this ?

Unfortunately to avoid any side effects with other mods, the user needs first to join the overworld so that all mods are able to sync their data.
As soon these data are synced the user could be transferred to the lobby dimension without any issues.

### Will there are 1.16.5 version ?

There are already a lot of dimension mods for 1.16.5 which are covering similar functionality like:

- <https://www.curseforge.com/minecraft/mc-mods/advanced-mining-dimension>
- <https://www.curseforge.com/minecraft/mc-mods/rftools-dimensions>
- <https://www.curseforge.com/minecraft/mc-mods/rftools>
- <https://www.curseforge.com/minecraft/mc-mods/aroma1997s-dimensional-world>
- <https://www.curseforge.com/minecraft/mc-mods/dimensionaldoors>
- <https://www.curseforge.com/minecraft/mc-mods/hunting-dimension>
- <https://www.curseforge.com/minecraft/mc-mods/ftb-team-islands-forge>

I see not really any reason why there should be "another" dimension mod for 1.16.5, which only provides the basic functionality.

### Will there are fabric version ?

Unfortunately I have no time to work on a separate fabric version.

## Version Status Overview 🛠️

| Version        | Status                |
| -------------- | --------------------- |
| Fabric Version | ❌ Not planned        |
| Forge 1.16.5   | ❌ Not planned        |
| Forge 1.17.1   | ❌ Not planned        |
| Forge 1.18.1   | ✔️ Active development |

## Note

Please only download the mod from the official CurseForge page or with the official CurseForge launcher like:

🏝 [Lobby, Fishing and Mining Dimension][mod_page]

If you are downloading this mod from other sources we could not make sure that it works as expected or does not includes any unwanted modification (e.g. adware, malware, ...).

[mod_page]: https://www.curseforge.com/minecraft/mc-mods/lobby
[fishing_dimension]: https://raw.githubusercontent.com/MarkusBordihn/BOs-Lobby/main/examples/fishing_dimension.png
[lobby_dimension]: https://raw.githubusercontent.com/MarkusBordihn/BOs-Lobby/main/examples/lobby_dimension.png
[mining_dimension]: https://raw.githubusercontent.com/MarkusBordihn/BOs-Lobby/main/examples/mining_dimension.png
