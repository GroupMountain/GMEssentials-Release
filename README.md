# 功能配置说明

## 配置文件结构
```json
{
    "version": 1,
    "features": {
        /* 功能模块配置 */
    },
    "commands": {
        /* 命令相关配置（当前版本暂未启用） */
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
```json
{
    "enable": false,
    "random": true,
    "seed": 0
}
```
- `enable`: 是否启用功能
- `random`: 是否生成随机种子
- `seed`: 指定固定种子（当random=false时生效）

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
```json
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
```json
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
- `explosionSetting`支持配置特定爆炸源的参数（如minecraft:creeper、minecraft:bed等）
- `defaultSetting`为默认参数，当`explosionSetting`中未指定特定爆炸源时，使用默认参数
- `allowExplosion`: 是否允许爆炸
- `maxRadius`: 最大爆炸半径
- `allowDestroy`: 是否允许破坏方块
- `allowFire`: 是否允许产生火焰
---

### 自定义命令别名 (custom_cmd_alias)
**功能**：为命令创建别名  
```json
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
**功能**：修复/gamemode 6命令支持
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
**配置值**：`true`/`false`

---

### 假人无需睡觉 (fake_player_no_sleep)
**功能**：睡觉时不会计算假人
**配置值**：`true`/`false`

---

### 隐藏OP标志 (invisible_op)
**功能**：看不见管理员的标志皇冠
**配置值**：`true`/`false`

---

### 未知方块清理 (cleaner_unknown_block)
**功能**: 加载区块时清理未知方块
**配置值**：`true`/`false`

---

## 命令模块列表

> 无

---

## UI模块列表

### 插件设置UI
**功能**：在设置界面添加插件设置选项
**配置值**: `true`/`false`

---