![English](https://img.shields.io/badge/English-inactive?style=for-the-badge)
[![中文](https://img.shields.io/badge/简体中文-informational?style=for-the-badge)](README.zh.md)

> [!WARNING]
> If you modify the configuration file, please reactivate or restart, do not reload this plugin at will.  
> The command is **ll reactivate GMEssentials**

# Function Configuration Description

## Configuration file structure

```jsonc
{
    "version": 1,
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

### Trusted_skin

**Function**: Allow players to display each other's skins normally  
**Configuration value**: `true`/`false`

---

### Force Education Edition (force_education_edition)

**Function**: Force to enable the educational version function (hot loading is not supported)  
**Configuration value**: `true`/`false`

---

### Force_achievements

**Function**: Allows achievements to be earned in archives that prohibit achievements  
**Configuration value**: `true`/`false`

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

**Function**: Scheduled execution of tasks

```jsonc
{
    "enable": false,
    "tasks": [
        {
            "cron": "0 0 0 * * ?",
            "task": "say scheduled task executed",
            "output": false
        }
    ]
}
```

- `enable`: whether to enable scheduled tasks
- `tasks`: Scheduled task list
  - `cron`: Scheduled task Cron expression
  - `task`: the command to execute
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

### Command Map (command_map)

**Function**: Register custom command mapping

```jsonc
{
    "enable": false,
    "map": {
        "gmc": {
            "command": "gamemode 1",
            "description": "Switch to creative mode",
            "permission": "GameDirectors"
        },
        "gms": {
            "command": "gamemode 0",
            "description": "Switch to survival mode",
            "permission": "GameDirectors"
        },
        "gma": {
            "command": "gamemode 2",
            "description": "Switch to adventure mode",
            "permission": "GameDirectors"
        },
        "gmsp": {
            "command": "gamemode spectator",
            "description": "Switch to spectator mode",
            "permission": "GameDirectors"
        }
    }
}
```

- `command`: the command to execute
- `description`: description of the command
- `permission`: the permission required to execute this command

> **Note**: The execution of the command is mandatory, regardless of whether the executor has the authority to execute the command, it will be enforced and ignore the permission check.

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
        "camera_aim_assist": false,
        "data_driven_biomes": false,
        "gametest": false,
        "jigsaw_structures": false,
        "third_person_cameras": false,
        "upcoming_creator_features": false,
        "villager_trades_rebalance": false,
        "y_2025_drop_1": false
    }
}
```

- `experiments`: List of experimental features
  - `camera_aim_assist`: Camera Aim Assist
  - `data_driven_biomes`: Data-Driven Biomes
  - `gametest`: GameTest Framework
  - `jigsaw_structures`: Data-Driven Jigsaw Structures
  - `third_person_cameras`: Creator Cameras: New Third-Person Presets
  - `upcoming_creator_features`: Upcoming Creator Features
  - `villager_trades_rebalance`: Villager Trade Rebalance
  - `y_2025_drop_1`: 2025 Drop 1

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

## UI module list

### Plugin Settings UI (server_settings)

**Function**: Add plugin setting options in the settings interface  
**Configuration value**: `true`/`false`

---
