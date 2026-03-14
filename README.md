# 🎮 Dust2 经典 FPS 游戏

一款基于 Three.js 的第一人称射击游戏，模拟经典 CS:GO 的 Dust2 地图和武器系统。

![Game Preview](https://img.shields.io/badge/Three.js-r128-green) ![License](https://img.shields.io/badge/License-MIT-blue)

---

## ✨ 功能特性

### 🗺️ 地图系统
- **Dust2 经典地图**：还原经典沙漠场景
- **动态沙漠地形**：程序化生成的沙丘起伏和纹理
- **真实碰撞检测**：玩家和敌人都无法穿墙

### 🔫 武器系统
- **AK-47**：高伤害突击步枪，支持连发
- **手枪**：精准的副武器
- **匕首**：近战武器，轻击和重击

### 🤖 敌人 AI
- **智能巡逻**：敌人在固定路线巡逻
- **追击玩家**：发现玩家后主动追击
- **攻击行为**：近距离攻击玩家
- **碰撞避障**：遇到障碍物自动绕行

### 🎯 战斗系统
- **真实后坐力**：射击时视角上跳，下蹲减少30%后坐力
- **爆头判定**：头部伤害加成
- **击杀反馈**：伤害数字、击杀通知、爆头提示

### 📊 UI 系统
- **血条显示**：动态颜色变化
- **弹药计数**：当前弹匣/备弹量
- **小地图**：实时显示玩家位置、敌人位置、建筑物轮廓
- **准星**：动态准星显示

---

## 🎮 操作说明

| 按键 | 功能 |
|------|------|
| `W` `A` `S` `D` | 移动 |
| `鼠标移动` | 瞄准/转向 |
| `鼠标左键` | 射击（支持连发） |
| `鼠标右键` | 瞄准镜 |
| `R` | 换弹 |
| `1` | 切换 AK-47 |
| `2` | 切换手枪 |
| `3` | 切换匕首 |
| `Shift` | 静步（无声慢走） |
| `Ctrl` | 下蹲 |
| `空格` | 跳跃 |
| `Ctrl + 空格` | 大跳 |

---

## 🔧 技术栈

- **3D 渲染**：Three.js r128
- **音效系统**：Web Audio API
- **样式**：原生 CSS
- **架构**：单文件 HTML 应用

### 核心技术实现

| 功能 | 技术方案 |
|------|----------|
| 3D 场景 | Three.js Scene + Camera + WebGLRenderer |
| 第一人称控制 | PointerLockControls + Euler 角度 |
| 碰撞检测 | AABB 包围盒 + Raycaster |
| 敌人 AI | 状态机（巡逻/追击/攻击） |
| 音效播放 | AudioContext + AudioBuffer |
| 小地图 | Canvas 2D 绘图 |

---

## 📁 项目结构

```
fps-game/
├── index.html          # 游戏主文件（包含所有代码）
├── assets/             # 音效资源
│   ├── footsteps.mp3   # 脚步声
│   ├── gunshot.mp3     # 枪声
│   ├── jump.mp3        # 跳跃声
│   └── ...
├── styles/
│   └── main.css        # 样式文件
└── README.md           # 项目说明
```

---

## 🚀 快速开始

### 方式一：直接运行
1. 下载 `index.html` 文件
2. 双击用浏览器打开
3. 点击"开始游戏"

### 方式二：本地服务器
```bash
# 使用 Python
python -m http.server 5000

# 或使用 Node.js
npx server -l 5000

# 访问 http://localhost:5000
```

---

## 🎯 游戏玩法

### 目标
消灭地图上的所有敌人，存活下来！

### 技巧
- **下蹲射击**：减少30%后坐力，提高精准度
- **静步移动**：无声接近敌人，发动突袭
- **爆头击杀**：头部伤害更高，快速消灭敌人
- **换弹时机**：注意弹药，及时换弹

---

## ⚙️ 配置参数

游戏中的关键参数（可在代码中修改）：

```javascript
// 玩家参数
const PLAYER_HEIGHT = 1.7;      // 玩家高度
const PLAYER_CROUCH_HEIGHT = 1.0; // 下蹲高度
const WALK_SPEED = 8;           // 行走速度
const SILENT_SPEED = 4;         // 静步速度

// 敌人参数
const ENEMY_SPEED = 3;          // 敌人移动速度
const ENEMY_ATTACK_RANGE = 2;   // 攻击范围
const ENEMY_ATTACK_DAMAGE = 10; // 攻击伤害

// 武器参数
const AK47_DAMAGE_BODY = 25;    // AK47身体伤害
const AK47_DAMAGE_HEAD = 100;   // AK47头部伤害
```

---

## 🐛 已知问题

- [ ] 音效依赖外部链接，离线可能无法播放
- [ ] 部分 GPU 可能存在渲染问题

---

## 📝 更新日志

### v1.0.0 (2024-03)
- ✅ 完整的 Dust2 地图
- ✅ AK-47、手枪、匕首三种武器
- ✅ 敌人 AI 系统
- ✅ 碰撞检测系统
- ✅ 小地图显示
- ✅ 血条和弹药 UI
- ✅ 沙漠地面材质

---

## 📄 许可证

MIT License - 可自由使用、修改和分发

---

## 🙏 致谢

- [Three.js](https://threejs.org/) - 3D 渲染引擎
- 音效来源：爱给网 (aigei.com)

---

**Enjoy the game! 🎮**
