![English](https://img.shields.io/badge/English-inactive?style=for-the-badge)
[![中文](https://img.shields.io/badge/简体中文-informational?style=for-the-badge)](README.zh.md)

> [!WARNING]
> If you modify the configuration file, please reactivate or restart, do not reload this plugin at will.  
> The command is **ll reactivate GMEssentials**

# Function Configuration Description

## Configuration file structure

```jsonc
{
    "version": 4,
    "log_level": "Info",
    "features": {
        /* Functional module configuration */
    },
    "ui": {
        /* UI related configuration */
    }
}
```

## Functional module list

### Basic Configuration

- `version`: configuration file version number
- `log_level`: log level (Trace, Debug, Info, Warn, Error, Fatal, Off)

---

### Fake seed (fake_seed)

**Function**: Hide the real server seed and show fake seeds to players  
**Configuration structure**:

```jsonc
{
    "enable": false,
    "random": true,
    "seed": 0
}
```

- `enable`: whether to enable the function
- `random`: whether to generate a random seed
- `seed`: specify a fixed seed (effective when random=false)

---

### Coexistence of resource packs (co_resource_pack)

**Function**: Allow client resource packs to be used in conjunction with server resource packs  
**Configuration value**: `true`/`false`

---

### Trusted_skin (trusted_skin)

**Function**: Allow players to display each other's skins normally  
**Configuration value**: `true`/`false`

---

### Force Education Edition (force_education_edition)

**Function**: Force to enable the educational version function (hot loading is not supported)  
**Configuration value**: `true`/`false`

---

### Force_achievements (force_achievements)

**Function**: Allows achievements to be earned in archives that prohibit achievements  
**Configuration value**: `true`/`false`

---

### Force-register Ability Command (force_register_ability_cmd)

**Feature**: Force-registers the `/ability` command  
**Config Value**: `true`/`false`

---

### Fake world name (fake_world_name)

**Function**: Customize the world name displayed to players

```jsonc
{
    "enable": false,
    "world_name": "§r§dCustom name"
}
```

---

### Automatic fishing (automatic_fishing)

**Function**: Automatically complete fishing operations  
**Configuration value**: `true`/`false`

---

### Explosion parameter modification (explosion_modify)

**Function**: Customize explosion behavior parameters

```jsonc
{
    "enable": false,
    "defaultSetting": {
        "allowExplosion": true,
        "maxRadius": 100.0,
        "allowDestroy": false,
        "allowFire": false
    },
    "explosionSetting": {
        "creeper": {
            "allowExplosion": false,
            "maxRadius": 5.0
        }
    }
}
```

- `explosionSetting` supports configuring parameters for specific explosion sources (such as minecraft:creeper, minecraft:bed, etc.)
- `defaultSetting` is the default parameter. When no specific explosion source is specified in `explosionSetting`, the default parameter is used.
- `allowExplosion`: whether explosion is allowed
- `maxRadius`: maximum explosion radius
- `allowDestroy`: whether to allow the destruction of blocks
- `allowFire`: whether to allow fire

---

### Custom command alias (custom_cmd_alias)

**Function**: Create aliases for commands

```jsonc
{
    "enable": false,
    "alias": {
        "gamemode": ["gm"],
        "teleport": ["tp"]
    }
}
```

---

### Custom Command Permissions (custom_cmd_permissions)

**Feature**: Overrides default command execution permissions

```jsonc
{
    "enable": false,
    "permissions": {
        "stop": "GameDirectors"
    }
}
```

- `permissions`: Custom permission levels for specific commands (e.g., `stop`, `give`)
  - `Any`: Players (can execute `/list`, `/me`, `/whisper`, etc.)
  - `GameDirectors`: Moderators (can execute `/clear`, `/fill`, `/give`, `/kill`, etc.)
  - `Admin`: Administrators (can execute `/op`, `/deop`, `/reload`, `/wsserver`, etc.)
  - `Host`: Server Host (can execute `/setmaxplayers`, etc.)
  - `Owner`: Console/Owner (can execute `/transfer`, `/stop`, `/save`, etc.)
  - `Internal`: Internal Tier (no functional difference from `Owner` identified yet)

---

### Double door (double_door)

**Function**: Automatically open and close adjacent doors synchronously  
**Configuration value**: `true`/`false`

---

### Fix gamemode 6 (gamemode6_fix)

**FEATURE**: Fixed /gamemode 6 command support  
**Configuration value**: `true`/`false`

---

### Disable setting interface modification permissions (block_modify_permissions)

**Function**: Disable the modification of permissions through the settings interface  
**Configuration value**: `true`/`false`

---

### Lock World Settings (lock_world_settings)

**Function**: Lock world settings  
**Configuration value**: `true`/`false`

---

### Right click to preview container (container_reader)

**Function**: When sneaking + empty-handed + right-clicking to open an unopenable container, an inoperable container will be opened for preview  
**Configuration value**: `true`/`false`

---

### Fast leaf decay (fast_leaf_decay)

**Function**: Leaves decay quickly

```jsonc
{
    "enable": false,
    "time": {
        "min": 10,
        "max": 20
    }
}
```

- `time`: Set the minimum and maximum time for leaves to decay (unit: tick)

---

### Fake player no need to sleep (fake_player_no_sleep)

**Function**: No dummies will be counted when sleeping  
**Configuration value**: `true`/`false`

---

### Hidden OP flag (invisible_op)

**Function**: Make the administrator's crown invisible  
**Configuration value**: `true`/`false`

---

### Unknown Block Cleaner (cleaner_unknown_block)

**Function**: Clean unknown blocks when loading chunks  
**Configuration value**: `true`/`false`

---

### Resource Pack Download Fix (resource_pack_download_fix)

**Function**: Fixed the issue that the client cannot download the server texture pack in some cases  
**Configuration value**: `true`/`false`

---

### Motd fake (fake_motd)

**Function**: Forged server Modd

```jsonc
{
    "enable": false,
    "motd": {
        "enable": false,
        "content": "§r§dCustom Motd"
    },
    "protocol_version": {
        "enable": false,
        "protocol_version": 758
    },
    "network_version": {
        "enable": false,
        "content": "1.21.60"
    },
    "player_count": {
        "enable": false,
        "player_count": 0
    },
    "max_player_count": {
        "enable": false,
        "max_player_count": 0
    },
    "guid": {
        "enable": false,
        "content": "Custom GUID"
    },
    "level_name": {
        "enable": false,
        "content": "Custom world name"
    },
    "game_mode": {
        "enable": false,
        "content": "Creative"
    },
    "local_port": {
        "enable": false,
        "local_port": 19132
    },
    "local_port_v6": {
        "enable": false,
        "local_port_v6": 19132
    },
    "other": {
        "enable": false,
        "content": ["Custom other information"]
    }
}
```

- `enable`: whether to enable forgery
- `motd`: Forge Motd
- `protocol_version`: fake protocol version
- `network_version`: fake network version
- `player_count`: fake the number of online players
- `max_player_count`: fake maximum number of players
- `guid`: forge GUID
- `level_name`: fake world name
- `game_mode`: fake game mode
  - `Survival`: Survival
  - `Creative`: Creation
  - `Adventure`: Adventure
  - `Spectator`: Spectator
  - `Default`: Default
- `local_port`: fake local port
- `local_port_v6`: fake local port V6
- `other`: fake other information

---

### Scheduled tasks (schedule_task)

**Function**: Scheduled execution of commands

```jsonc
{
    "enable": false,
    "tasks": [
        {
            "cron": "0 0 0 * * ?",
            "commands": [
                "say scheduled task executed"
            ],
            "output": false
        }
    ]
}
```

- `enable`: whether to enable scheduled tasks
- `tasks`: Scheduled task list
  - `cron`: Scheduled task Cron expression
  - `commands`: the commands to execute
  - `output`: Whether the console outputs the task execution results

---

### Quick Command GUI (quick_cmd_gui)

**Function**: Add GUI to the original command

```jsonc
{
    "enable": false,
    "commands": {
        "gamemode": false,
        "difficulty": false,
        "time": false,
        "weather": false,
        "kick": false,
    }
}
```

---

### Command Mapping (command_map)

**Feature**: Registers custom command mappings

```jsonc
{
    "enable": false,
    "commands": [
        {
            "command": "test",
            "description": "Test command",
            "run_commands": [
                {
                    "command": "say Test command executed, input: $1, enum: $2",
                    "output": true
                }
            ],
            "permission": "Any",
            "params": [
                {
                    "name": "message",
                    "type": "String",
                    "optional": false
                },
                {
                    "name": "enum",
                    "type": "Enum",
                    "optional": false,
                    "enum_name": "gmessentials_test_enum",
                    "choices": [
                        "A",
                        "B",
                        "C"
                    ]
                }
            ]
        }
    ]
}
```

- `command`: Command to register
- `description`: Command description
- `run_commands`: List of commands to execute
  - `command`: Command to execute (supports `$0` for command name, `$1` for first parameter, etc.)
  - `output`: Whether to output command execution results
- `permission`: Permission required to register/use the command
- `params`: Parameter list
  - `name`: Parameter name
  - `type`: Parameter type
    - `Int`: Integer
    - `Bool`: Boolean
    - `Float`: Floating-point number
    - `Dimension`: Dimension name
    - `String`: String
    - `Enum`: Enumeration value
    - `SoftEnum`: Dynamic enumeration
    - `Actor`: Entity
    - `Player`: Player
    - `BlockPos`: Integer coordinates
    - `Vec3`: Floating-point coordinates
    - `RawText`: Raw text (differs from String)
    - `JsonValue`: JSON value
    - `Item`: Item type
    - `BlockName`: Block type
    - `BlockState`: Block state
    - `Effect`: Effect type
    - `ActorType`: Entity type
    - `Command`: Command (used for subcommands like `execute run`)
  - `optional`: Whether the parameter is optional
  - `enum_name`: Enumeration name (required for `Enum`/`SoftEnum` types)
  - `choices`: Enumeration value list (optional for `Enum`/`SoftEnum` types)

> **Note**: Commands in `run_commands` are **forcibly executed** regardless of the executor's permissions. Permission checks are ignored.

---

### Farmland protection (farm_land_protect)

**Function**: Protect farmland from being trampled and turned into mud  
**Configuration value**: `true`/`false`

---

### Dynamic Motd (dynamic_motd)

**Function**: Dynamically switch and update Modd

```jsonc
{
    "enable": true,
    "update_interval": 2500,
    "content": [
        "Welcome to the server!",
        "This is a dynamic motd example.",
        "The motd will be updated every 2.5 seconds.",
        "current version: ${papi:server_version}"
    ]
}
```

- `enable`: whether to enable dynamic Modd
- `update_interval`: the time interval for updating Modd (unit: milliseconds)
- `content`: Motd content list (supports PAPI variables)

---

### Automatic item replenishment (auto_reload)

**Function**: Automatically replenish items when they are used up  
**Configuration value**: `true`/`false`

---

### Death Loot by Dimension (death_loot_dimension)

**_Feature_**: Controls item drop on death in different dimensions

```jsonc
{
    "enable": false,
    "dimensions": {
        "overworld": false,
        "nether": false,
        "the end": false
    }
}
```

- `dimensions`: Dimension list (supports custom dimensions)
  - `overworld`: Overworld
  - `nether`: Nether
  - `the end`: The End

> **Note**: The dimension keys represent `whether to enable keep inventory` (prevent item drops) instead of controlling whether items drop.

---

### Chat Record (chat_record)

**Feature**: Logs chat history, allowing players to view previous chats after rejoining the server.

```jsonc
{
    "enable": false,
    "max_record": 50
}
```

- `max_record`: Maximum number of chat entries stored

---

### Experiments Editor (experiments_editor)

**Feature**: Edit experimental gameplay features

```jsonc
{
    "enable": false,
    "experiments": {
        "TestExperiment": false,
        "NextUpdate": false,
        "DisabledExperiment": false,
        "ExperimentalText": false,
        "AllowSeedChange": false,
        "DataDrivenBiomes": false,
        "UpcomingCreatorFeatures": false,
        "BetaApis": false,
        "DataDrivenVanillaBlocksAndItems": false,
        "DisableDataDrivenVanillaBlocksAndItems": false,
        "ExperimentalCreatorCameras": false,
        "MinecraftExplorer": false,
        "DeferredTechnicalPreview": false,
        "VillagerTradesRebalance": false,
        "VanillaBlockGeometry": false,
        "JigsawStructures": false,
        "SimplifiedSpawnRules": false
    }
}
```

- `experiments`: List of experimental features

---

### Addon Loader (addon_loader)

**Feature**: Simplifies addon loading

```jsonc
{
    "enable": false,
    "directory": [
        "./addons"
    ]
}
```

- `directory`: List of directories to load addons from
  - All folders and files with extensions like `.zip`, `.mcpack`, or `.mcaddon` in these directories will be automatically loaded.

---

### Chat Formatter (chat_formatter)

**Feature**: Customizes chat message formatting

```jsonc
{
    "enable": true,
    "format": {
        "default": "<${papi:player_realname}> ${message}",
        "zh_CN": "<${papi:player_realname}> ${message}",
        "en_US": "<${papi:player_realname}> ${message}"
    }
}
```

- `format`: Chat format rules
  - `default`: Default chat format
  - `...`: Language-specific formats (e.g., `zh_CN`, `en_US`)

> **Note**: Supports PAPI placeholders and multilingual formatting, _if_ the referenced PAPI variables have multilingual capabilities.

---

### Buff Blacklist (ban_buff)

**Feature**: Disables specified buffs/effects

```jsonc
{
    "enable": false,
    "buffs": [
        "infested"
    ]
}
```

- `buffs`: List of buff/effect IDs to disable

---

### Dimension-based Command Restrictions (dimension_disabling_command)

**Feature**: Disables specified commands in specific dimensions

```jsonc
{
    "enable": false,
    "dimensions": {
        "overworld": ["tell"],
        "nether": ["me"],
        "the end": ["list"]
    }
}
```

- `dimensions`: Dimension list (supports custom dimensions)
  - `overworld`: Overworld
  - `nether`: Nether
  - `the end`: The End

---

### Entity Restrictions (ban_entity)

**Feature**: Disables specified entities

```jsonc
{
    "enable": false,
    "entities": {
        "minecraft:silverfish": {
            "load": false,
            "spawn": true,
            "place": false,
            "summon": false
        }
    }
}
```

- `entities`: Entity restriction list
  - `load`: Load from save
  - `spawn`: Natural spawning
  - `place`: Spawning via spawn egg
  - `summon`: Summon via command

---

### XP Orb Merging (xp_orb_merge)  

**Feature**: Merges nearby experience orbs  

```jsonc  
{  
    "enable": false,  
    "radius": 3.0,  
    "time": 20  
}  
```  

- `radius`: Merge radius (合并半径)  
- `time`: Interval between merge operations (in ticks) (多久执行一次合并操作，单位：刻)  

---

## UI module list

### Plugin Settings UI (server_settings)

**Function**: Add plugin setting options in the settings interface  
**Configuration value**: `true`/`false`

---
