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
    "log_level": "Info",
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
- `log_level`: 日志级别 (Trace, Debug, Info, Warn, Error, Fatal, Off)

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

### 强制注册 Ability 命令 (force_register_ability_cmd)

**功能**：强制注册 /ability 命令
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

### 自定义命令权限 (custom_cmd_permissions)

**功能**：强制修改命令执行所需权限

```jsonc
{
    "enable": false,
    "permissions": {
        "stop": "GameDirectors"
    }
}
```

- `permissions`支持配置特定命令的权限（如 stop、give 等）
  - `Any`: 玩家(可以执行 /list,/me,/w 等命令)
  - `GameDirectors`: 管理员(可以执行 /clear,/fill,/give,/kill 等命令)
  - `Admin`: 管理员(可以执行 /op,/deop,/reload,/wsserver 等命令)
  - `Host`: 房主(可以执行 /setmaxplayers 等命令)
  - `Owner`: 控制台(可以执行 /transfer,/stop,/save 等命令)
  - `Internal`: 内部权限(暂未发现和 Owner 权限的区别)

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

**功能**：定时执行命令

```jsonc
{
    "enable": false,
    "tasks": [
        {
            "cron": "0 0 0 * * ?",
            "command": "say 定时任务执行了",
            "output": false
        }
    ]
}
```

- `enable`: 是否启用定时任务
- `tasks`: 定时任务列表
  - `cron`: 定时任务 Cron 表达式
  - `command`: 执行的命令
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
    "commands": [
        {
            "command": "test",
            "description": "测试命令",
            "run_commands": [
                {
                    "command": "say 测试命令执行了, 输入内容: $1, 枚举值: $2",
                    "output": true,
                    "permission": "Any"
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

- `command`: 要注册的命令
- `description`: 命令描述
- `run_commands`: 执行的命令列表
  - `command`: 执行的命令(支持参数替换$0 为命令名, $1 为第一个参数, $2 为第二个参数, 以此类推)
  - `output`: 是否输出命令执行结果
  - `permission`: 执行命令所需的权限
- `permission`: 注册执行命令所需的权限
- `params`: 参数列表
  - `name`: 参数名称
  - `type`: 参数类型
    - `Int`: 整数
    - `Bool`: 布尔值
    - `Float`: 浮点数
    - `Dimension`: 维度名
    - `String`: 字符串
    - `Enum`: 枚举值
    - `SoftEnum`: 可变枚举
    - `Actor`: 实体
    - `Player`: 玩家
    - `BlockPos`: 整数坐标
    - `Vec3`: 浮点数坐标
    - `RawText`: 原始文本(和 String 不一样)
    - `JsonValue`: JSON 值
    - `Item`: 物品类型
    - `BlockName`: 方块类型
    - `BlockState`: 方块状态
    - `Effect`: 效果类型
    - `ActorType`: 实体类型
    - `Command`: 命令(用于子命令，如 execute 的 run)
  - `optional`: 是否可选
  - `enum_name`: 枚举名称(当参数类型为 Enum 或 SoftEnum 时必填)
  - `choices`: 枚举值列表(当参数类型为 Enum 或 SoftEnum 时可选)

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

**功能**：控制不同维度死亡是否掉落物品

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
  - 在目录下的文件夹和 zip, mcpack, mcaddon

---

### 聊天格式化 (chat_formatter)

**功能**：自定义聊天格式

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

- `format`: 聊天格式列表
  - `default`: 默认聊天格式
  - `...`: 其他语言聊天格式 (例如: `zh_CN`, `en_US`)

> **注意**: 支持 papi 多语言翻译，前提是 papi 变量支持。

---

### Buff 禁用 (ban_buff)

**功能**：禁用某些 Buff

```jsonc
{
    "enable": false,
    "buffs": [
        "infested",
    ]
}
```

---

### 维度命令禁用 (dimension_disabling_command)

**功能**：在特定维度下禁用某些命令

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

- `dimensions`: 维度列表(支持自定义维度)
  - `overworld`: 主世界
  - `nether`: 下界
  - `the end`: 末地

---

### 实体禁用 (ban_entity)

**功能**：禁用某些实体

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

- `entities`: 实体列表
  - `load`: 从存档中加载
  - `spawn`: 自然生成
  - `place`: 生物蛋放置
  - `summon`: 命令召唤

---

### 经验球合并 (xp_orb_merge)

**功能**：合并相近的经验球

```jsonc
{
    "enable": false,
    "radius": 3.0,
    "time": 20
}
```

- `radius`: 合并半径
- `time`: 多久执行一次合并操作(单位:刻)

---

## UI 模块列表

### 插件设置 UI (server_settings)

**功能**：在设置界面添加插件设置选项  
**配置值**: `true`/`false`

---
