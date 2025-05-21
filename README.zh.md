[![English](https://img.shields.io/badge/English-informational?style=for-the-badge)](README.md)
![中文](https://img.shields.io/badge/简体中文-inactive?style=for-the-badge)

> [!WARNING]
> 如果修改了配置文件，请重新激活或者重启，不要随意重载此插件。  
> 指令为**ll reactivate GMEssentials**

# 功能配置说明

## 配置文件结构

```jsonc
{
    "version": 1,
    "features": {
        /* 功能模块配置 */
    },
    "ui": {
        /* UI相关配置 */
    }
}
```

## 功能模块列表

### 基础配置

- `version`: 配置文件版本号

---

### 假种子 (fake_seed)

**功能**：隐藏服务器真实种子，向玩家显示伪造的种子  
**配置结构**：

```jsonc
{
    "enable": false,
    "random": true,
    "seed": 0
}
```

- `enable`: 是否启用功能
- `random`: 是否生成随机种子
- `seed`: 指定固定种子（当 random=false 时生效）

---

### 材质包共存 (co_resource_pack)

**功能**：允许客户端资源包与服务端资源包叠加使用  
**配置值**：`true`/`false`

---

### 信任皮肤 (trusted_skin)

**功能**：允许玩家正常显示彼此皮肤  
**配置值**：`true`/`false`

---

### 强制教育版 (force_education_edition)

**功能**：强制开启教育版功能（不支持热加载）  
**配置值**：`true`/`false`

---

### 强制成就 (force_achievements)

**功能**：允许在禁止成就的存档中获得成就  
**配置值**：`true`/`false`

---

### 假存档名 (fake_world_name)

**功能**：自定义显示给玩家的世界名称

```jsonc
{
    "enable": false,
    "world_name": "§r§d自定义名称"
}
```

---

### 自动钓鱼 (automatic_fishing)

**功能**：自动完成钓鱼操作  
**配置值**：`true`/`false`

---

### 爆炸参数修改 (explosion_modify)

**功能**：自定义爆炸行为参数

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

- `explosionSetting`支持配置特定爆炸源的参数（如 minecraft:creeper、minecraft:bed 等）
- `defaultSetting`为默认参数，当`explosionSetting`中未指定特定爆炸源时，使用默认参数
- `allowExplosion`: 是否允许爆炸
- `maxRadius`: 最大爆炸半径
- `allowDestroy`: 是否允许破坏方块
- `allowFire`: 是否允许产生火焰

---

### 自定义命令别名 (custom_cmd_alias)

**功能**：为命令创建别名

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

### 双开门 (double_door)

**功能**：自动同步开关相邻的门  
**配置值**：`true`/`false`

---

### 修复 gamemode 6 (gamemode6_fix)

**功能**：修复/gamemode 6 命令支持  
**配置值**：`true`/`false`

---

### 禁止设置界面修改权限 (block_modify_permissions)

**功能**：禁止通过设置界面修改权限  
**配置值**：`true`/`false`

---

### 锁定世界设置 (lock_world_settings)

**功能**：锁定世界设置  
**配置值**：`true`/`false`

---

### 潜行右键预览容器 (container_reader)

**功能**：潜行+空手+右键打开打不开的容器时,会打开一个无法操作的容器,用于预览  
**配置值**：`true`/`false`

---

### 树叶快速腐烂 (fast_leaf_decay)

**功能**：树叶快速腐烂

```jsonc
{
    "enable": false,
    "time": {
        "min": 10,
        "max": 20
    }
}
```

- `time`：设置树叶腐烂的最小和最大时间(单位:刻)

---

### 假人无需睡觉 (fake_player_no_sleep)

**功能**：睡觉时不会计算假人  
**配置值**：`true`/`false`

---

### 隐藏 OP 标志 (invisible_op)

**功能**：看不见管理员的标志皇冠  
**配置值**：`true`/`false`

---

### 未知方块清理 (cleaner_unknown_block)

**功能**: 加载区块时清理未知方块  
**配置值**：`true`/`false`

---

### 材质包下载修复 (resource_pack_download_fix)

**功能**：修复某些情况下客户端无法下载服务端材质包的问题  
**配置值**：`true`/`false`

---

### Motd 伪造 (fake_motd)

**功能**：伪造服务器 Motd

```jsonc
{
    "enable": false,
    "motd": {
        "enable": false,
        "content": "§r§d自定义Motd"
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
        "content": "自定义GUID"
    },
    "level_name": {
        "enable": false,
        "content": "自定义世界名称"
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
        "content": ["自定义其他信息"]
    }
}
```

- `enable`: 是否启用伪造
- `motd`: 伪造 Motd
- `protocol_version`: 伪造协议版本
- `network_version`: 伪造网络版本
- `player_count`: 伪造在线玩家数量
- `max_player_count`: 伪造最大玩家数量
- `guid`: 伪造 GUID
- `level_name`: 伪造世界名称
- `game_mode`: 伪造游戏模式
  - `Survival`: 生存
  - `Creative`: 创造
  - `Adventure`: 冒险
  - `Spectator`: 旁观者
  - `Default`: 默认
- `local_port`: 伪造本地端口
- `local_port_v6`: 伪造本地端口 V6
- `other`: 伪造其他信息

---

### 定时任务 (schedule_task)

**功能**：定时执行任务

```jsonc
{
    "enable": false,
    "tasks": [
        {
            "cron": "0 0 0 * * ?",
            "task": "say 定时任务执行了",
            "output": false
        }
    ]
}
```

- `enable`: 是否启用定时任务
- `tasks`: 定时任务列表
  - `cron`: 定时任务 Cron 表达式
  - `task`: 执行的命令
  - `output`: 控制台是否输出任务执行结果

---

### 快捷命令 GUI (quick_cmd_gui)

**功能**：给原版命令添加 GUI

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

### 命令映射 (command_map)

**功能**：注册自定义命令映射

```jsonc
{
    "enable": false,
    "map": {
        "gmc": {
            "command": "gamemode 1",
            "description": "切换为创造模式",
            "permission": "GameDirectors"
        },
        "gms": {
            "command": "gamemode 0",
            "description": "切换为生存模式",
            "permission": "GameDirectors"
        },
        "gma": {
            "command": "gamemode 2",
            "description": "切换为冒险模式",
            "permission": "GameDirectors"
        },
        "gmsp": {
            "command": "gamemode spectator",
            "description": "切换为旁观者模式",
            "permission": "GameDirectors"
        }
    }
}
```

- `command`: 要执行的命令
- `description`: 命令的描述
- `permission`: 执行此命令所需的权限

> **注意**：执行命令是强制执行的，无论执行者对执行的命令是否有权限，都会强制执行，无视权限检测。

---

### 耕地防踩 (farm_land_protect)

**功能**：保护耕地不被踩踏变成泥土  
**配置值**：`true`/`false`

---

### 动态 Motd (dynamic_motd)

**功能**：动态切换更新 Motd

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

- `enable`: 是否启用动态 Motd
- `update_interval`: 更新 Motd 的时间间隔(单位:毫秒)
- `content`: Motd 内容列表(支持 PAPI 变量)

---

### 物品自动补充 (auto_reload)

**功能**：手上物品用光时自动补充  
**配置值**：`true`/`false`

---

### 指定维度死亡掉落 (death_loot_dimension)

**\*功能**：控制不同维度死亡是否掉落物品

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

- `dimensions`: 维度列表(支持自定义维度)
  - `overworld`: 主世界
  - `nether`: 下界
  - `the end`: 末地

> **注意**：维度键值为`是否开启死亡不掉落`，而不是是否掉落

---

### 聊天记录 (chat_record)

**功能**：记录聊天记录，玩家退出服务器后重进服务器可以查看聊天记录

```jsonc
{
    "enable": false,
    "max_record": 50
}
```

- `max_record`: 最大记录条数

---

### 实验玩法编辑 (experiments_editor)

**功能**：编辑实验玩法

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

- `experiments`: 实验玩法列表
  - `camera_aim_assist`: 瞄准辅助
  - `data_driven_biomes`: 自定义生物群系
  - `gametest`: 测试 API
  - `jigsaw_structures`: 数据驱动拼图结构
  - `third_person_cameras`: 创作者相机：新的第三人称预设
  - `upcoming_creator_features`: 即将推出的创作者功能
  - `villager_trades_rebalance`: 村民贸易再平衡
  - `y_2025_drop_1`: 2025 年第一次更新

---

### Addon 加载 (addon_loader)

**功能**：快捷加载 Addon

```jsonc
{
    "enable": false,
    "directory": [
        "./addons"
    ]
}
```

- `directory`: Addon 加载目录列表
  - 在目录下的文件夹和 zip, mcpack, mcaddon 等后缀文件都会被尝试加载

---

## UI 模块列表

### 插件设置 UI (server_settings)

**功能**：在设置界面添加插件设置选项  
**配置值**: `true`/`false`

---
