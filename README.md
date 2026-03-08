# sts2_typing

**游戏内聊天 Mod，适用于 Slay the Spire 2**  
**In-game chat mod for Slay the Spire 2**

实时发送消息、分享 Emoji，并将卡牌、遗物、药水、能力以可交互链接的形式直接插入聊天框。

Send messages in real time, share Emoji, and insert cards, relics, potions, and powers as interactive links directly into chat.

---

## 功能 / Features

| | 中文 | English |
|---|---|---|
| 💬 | 聊天面板悬浮于屏幕角落，不操作时自动淡出 | Floating chat panel in the corner; fades out when idle |
| 🔗 | `Alt + 左键` 任意物品，生成带悬停预览的可点击链接 | `Alt + Left-click` any item to insert a hoverable link |
| 😄 | 内置 18 个 Emoji（由 [Lucide](https://lucide.dev) 提供） | 18 built-in Emoji icons via [Lucide](https://lucide.dev) |
| 🌐 | 消息通过游戏内置网络广播给所有在线玩家 | Messages broadcast to all connected players over the built-in network |
| ⌨️ | 键盘优先：`Enter` 打开 / 发送，`Esc` 关闭 | Keyboard-first: `Enter` to open/send, `Esc` to close |

---

## 快捷键 / Keybindings

| 操作 / Action | 按键 / Key |
|---|---|
| 打开聊天框 / Open chat | `Enter` |
| 发送消息 / Send message | `Enter` |
| 关闭聊天框或 Emoji 选择器 / Close chat or Emoji picker | `Esc` |
| 分享悬停的物品 / Share hovered item | `Alt + Left-click` |
| 打开 Emoji 选择器 / Open Emoji picker | 点击输入框内的 Emoji 按钮 / Click the Emoji button in the input box |

---

## 安装 / Installation

1. 从 [最新 Release](https://github.com/Shiroim/sts2_typing/releases/latest) 下载 `typing.zip`  
   Download `typing.zip` from the [latest release](https://github.com/Shiroim/sts2_typing/releases/latest)

2. 解压到游戏的 Mods 文件夹  
   Extract into the game's Mods folder:
   ```
   <Steam library>/steamapps/common/Slay the Spire 2/Mods/
   ```

3. 启动游戏，在 Mod 菜单中启用即可  
   Launch the game and enable the mod in the Mod menu

---

## 从源码构建 / Building from Source

**环境要求 / Requirements**

- [.NET SDK](https://dotnet.microsoft.com/download)（版本与游戏目录中 `global.json` 一致 / matching the version in the game's `global.json`）
- 支持 .NET 的 [Godot 4](https://godotengine.org/) / Godot 4 with .NET support
- Slay the Spire 2 游戏本体（编译时需引用游戏程序集 / needed to reference game assemblies）

**步骤 / Steps**

```bash
# 1. 克隆仓库 / Clone the repo
git clone https://github.com/Shiroim/sts2_typing.git

# 2. 按需修改 typing.csproj 中的游戏路径
#    Edit the game path reference in typing.csproj if needed

# 3. 构建 / Build
dotnet build
```

构建完成后，通过 Godot 导出，或将 `.pck` / `.dll` 手动复制到 Mods 文件夹。  
After building, export via Godot or copy the `.pck` / `.dll` to the Mods folder manually.

---

## 物品链接格式 / Item Link Format

物品链接以 `{{type:id}}` 格式编码于消息文本中，渲染为带样式的可交互文字。  
Item links are encoded as `{{type:id}}` in message text and rendered as styled interactive spans.

| 类型 / Type | 示例 / Example |
|---|---|
| 卡牌 / Card | `{{card:MegaCrit.Sts2.Cards.Strike:0}}` |
| 药水 / Potion | `{{potion:MegaCrit.Sts2.Potions.FirePotion}}` |
| 遗物 / Relic | `{{relic:MegaCrit.Sts2.Relics.BurningBlood}}` |
| 能力 / Power | 通过 `Alt + 左键` 自动插入 / Auto-inserted via `Alt + Left-click` |
| 目标生物 / Creature | 通过 `Alt + 左键` 自动插入 / Auto-inserted via `Alt + Left-click` |

---

## 开源协议 / License

本项目基于 [MIT License](LICENSE) 开源。  
This project is licensed under the [MIT License](LICENSE).

图标来自 [Lucide](https://lucide.dev)，使用 ISC License 授权。部分版权归 Cole Bemis 2013–2026 所有（源自 Feather，MIT 协议）。  
Icons from [Lucide](https://lucide.dev), licensed under ISC. Portions copyright Cole Bemis 2013–2026 (derived from Feather, MIT).

---

*本 Mod 与 MegaCrit 官方无关，亦未获得官方背书。*  
*This mod is not affiliated with or endorsed by MegaCrit.*
