# Cyclops Restored — Subnautica 2 独眼巨人号还原 Mod

**这是《Subnautica 2：异星水域》（深海迷航 2）的非官方大型潜艇 Mod。** 它将一代的独眼巨人号适配到二代，提供制造、驾驶、可步行船舱、储物、升级模块、舱内设施和蝌蚪号停靠功能。需要安装 Subnautica 2 游戏本体。[适用游戏 / Base game](https://store.steampowered.com/app/1962700/Subnautica_2/)

**Cyclops Restored is an unofficial mod for Subnautica 2.** It brings the Cyclops submarine from the first game into the sequel, with construction, piloting, walkable interiors, storage, upgrades, interior facilities and Tadpole docking. It requires the Subnautica 2 base game; it is not a mod for the first Subnautica or Below Zero.

**第二个公开测试版 / Second public beta: `v0.9.0-beta.2`**

[下载 / Downloads](https://github.com/raevenkelby6674-byte/SN2-CyclopsRestored/releases/tag/v0.9.0-beta.2) · [反馈问题 / Report a bug](https://github.com/raevenkelby6674-byte/SN2-CyclopsRestored/issues)

## 适用版本与测试状态 / Compatibility

| 项目 / Item | 说明 / Details |
| --- | --- |
| 游戏 / Game | Subnautica 2，Windows Steam，`0.1.2.3-131439` |
| 加载器 / Loader | UE4SS `v3.0.1 Beta #0`，提交 / commit `1ba38db4`；测试所用包 / tested package `3.0.1-1176-g1ba38db4` |
| 模式 / Modes | 单人；主机开房与加入者的实验性多人支持 / Single-player; experimental host-and-join co-op |
| 构建 / Build | 公开版本 beta.2 对应内部构建 `0.9.0-beta.13-mp-test`；安装文件保持相同 / Public beta.2 uses the unchanged beta.13 internal build |

**多人默认允许每位玩家使用完整功能，不设置船主或管理员专属权限。** 驾驶位仍遵守占用规则，物品操作仍遵守容量和资源规则。所有参与者必须安装相同的 Mod 和配套加载器。已完成离线主机／加入者回放与打包核验，**尚未完成两台电脑的真实联机验收**，专用服务器也未验证。

All players have access to the full feature set, subject to normal seat occupancy, capacity and resource rules. Every participant needs the same mod and compatible loader. Host/client offline replays and package checks passed; **real two-machine co-op and dedicated servers have not been validated**. This remains a prerelease, not a stability guarantee.

## 本版更新 / What's new since public beta.1

- **驾驶与交互：** 修正会反复中断整船更新、关闭推进和交互的脚本错误；改进退出驾驶、关闭编辑面板及切换存档后的输入清理。
- **声呐与信标：** 修正信标初始化和声呐／驾驶台效果加载路径；声呐排除自身船舱和近处人物。
- **储物与模块：** 修正原生物品数量处理、存取失败、中键数量选择和模块类型判定；保留原柜子布局，储物压缩模块上限为 **32 / 64 / 128**。
- **名称与外观：** 柜名直接替换原 `LOCK` 铭牌文字；外观编辑支持点击选色、舱门配色和可拖动旋转的半透明 3D 预览。船名用于信标，船壳不显示名称。
- **动力与回收：** 补充外部螺旋桨运动、生命值清零后的炸毁／残骸与物资回收。残骸保留物资和模块；柜子每个占用格的物资可归档为一个压缩球，保留数量和物品数据。
- **整船多人适配：** 覆盖驾驶、设施建造与供电、模块、储物、停靠、配色、舱门和残骸回收；主机结算共享物资、耗电和伤害，界面与输入归实际操作的玩家。

Since public beta.1: repairs to the ship update loop, driving/input cleanup, sonar loading and self-exclusion, beacon setup, native inventory counts and transfers, quantity selection and module filtering. Locker names replace the original nameplate, and customization adds click selection, hatch colors and a rotatable translucent preview. Propeller motion, wreck/cargo recovery and experimental whole-mod co-op are included.

**压缩球规则：** 仅在实际放入完好独眼的储物柜时自动检查一次。能完整还原才解包；空间不足时保留压缩球，取出后再放入可重试。还原遵守该船当前的储物压缩等级，未安装模块时按普通容量处理；不会持续轮询或强行塞入物品。

**Cargo spheres:** one unpack attempt per actual insertion into an intact Cyclops locker. Unpacking is all-or-nothing and respects the receiving ship's current stacking tier. Insufficient space leaves the sphere intact; remove and reinsert to retry. There is no continuous unpack polling.

## 下载哪个文件 / Which file to download

- **`CyclopsRestored-v0.9.0-beta.2-Win64.zip`**：玩家安装包，包含内容插件、Lua 脚本和原生供电桥。/ Install this to play.
- **`CyclopsRestored-v0.9.0-beta.2-Source.zip`**：自编代码、翻译及开发说明，供开发者查看。/ Original mod code, translations and development notes.
- **两个 `.sha256` 文件**：对应 ZIP 的 SHA-256 校验值。/ Checksums for the two ZIPs.

只玩游戏下载 Win64 包即可。源码包及 GitHub 自动生成的 `Source code` 压缩包都不能代替安装包。UE4SS 需单独安装。

Players only need the Win64 ZIP. Neither the explicit Source ZIP nor GitHub's automatic source archives are install packages. UE4SS is a separate dependency.

## 安装与更新 / Installation and update

1. **完全退出游戏并备份存档。** Steam 库 → 右键 Subnautica 2 → 管理 → 浏览本地文件，打开包含 `Subnautica2.exe` 和 `Subnautica2` 文件夹的游戏根目录。
2. **安装配套 UE4SS。** [上游下载页](https://github.com/UE4SS-RE/RE-UE4SS/releases/tag/experimental-latest) · [安装文档](https://docs.ue4ss.com/dev/installation-guide.html)。本版测试使用上表中的构建，其他构建未验证。将加载器的 `dwmapi.dll` 和 `ue4ss` 文件夹放到 `<游戏根目录>/Subnautica2/Binaries/Win64/`，与 `Subnautica2-Win64-Shipping.exe` 同级。已有兼容加载器可保留。
3. **更新旧版时，先移出旧 Mod。** 将下面两个 `CyclopsRestored` 文件夹备份到游戏目录之外，再安装新包，避免残留脚本或旧 Pak 混用。不要删除存档、整个 `Mods` 文件夹、加载器或其他 Mod。
4. **安装新包。** 解压 `CyclopsRestored-v0.9.0-beta.2-Win64.zip`，把其中的 `Subnautica2` 文件夹合并到**游戏根目录**。内容插件与脚本必须同时安装；不要把整个 ZIP 解压进 `Win64`，也不要多套一层版本号文件夹。
5. **启动使用。** 从 Steam 启动游戏，使用栖息所建造器放置“海面载具建造平台”，在开阔深水处通过平台屏幕制造独眼。联机时所有玩家先完成相同更新，再由主机开房、其他玩家加入。

```text
<游戏根目录> / <game root>
├─ Subnautica2.exe
└─ Subnautica2
   ├─ Mods/CyclopsRestored
   │  ├─ CyclopsRestored.uplugin
   │  └─ Content/Paks/Windows/  (.pak + .utoc + .ucas)
   └─ Binaries/Win64
      ├─ Subnautica2-Win64-Shipping.exe
      ├─ dwmapi.dll                         [UE4SS]
      └─ ue4ss
         ├─ UE4SS.dll                       [UE4SS]
         └─ Mods/CyclopsRestored
            ├─ enabled.txt
            ├─ Scripts/main.lua
            └─ native/CyclopsFinitePower.dll
```

**English:** Fully exit the game and back up your save. In Steam, select Manage → Browse local files. Install the tested UE4SS build beside the shipping executable using the layout above. For an update, move only the two old `CyclopsRestored` folders outside the game directory, then merge the new ZIP's `Subnautica2` folder into the game root. Keep saves, the loader and other mods. Start through Steam; build a Mobile Vehicle Bay with the Habitat Builder and use its screen in deep open water. For co-op, update every player's installation before hosting/joining.

## 已知问题与反馈 / Known issues and reporting

- 柜名显示和自定义外观已有修正，但旧存档、不同分辨率与联机显示仍需更多实测；不宣称完全消除所有显示问题。
- 偶发输入锁定、退出驾驶与编辑后交互恢复仍是重点回归项。若出现只能按 Esc、人物无法移动或交互，请保留日志后完全退出游戏再启动；仅退到主菜单可能保留进程状态。
- 多人驾驶交接、同时存取、重连、供电、建造及炸毁回收仍需真实联机测试。建议先用备份存档测试。
- 目前只针对上述游戏构建核验。游戏更新后需重新确认兼容性，勿绕过原生桥版本校验。

Locker labels and customization include fixes but still need broader old-save, resolution and co-op testing. Intermittent input lock remains a regression focus. If only Esc works, preserve the log and fully restart the game. Co-op handoff, simultaneous transfers, reconnects, power, construction and wreck recovery need real-session testing. Other game builds are not validated.

反馈时请附：游戏与 Mod 版本、单人／主机／加入者身份、触发步骤和相关日志。日志位置：`Subnautica2/Binaries/Win64/ue4ss/UE4SS.log`。上传前检查个人信息；无需上传整份存档或游戏文件。

For bug reports, include the game/mod version, solo/host/client role, reproduction steps and relevant `UE4SS.log` lines. Review personal information before posting; full saves or game archives are not required.

## 语言、校验与源码 / Languages, checksums and source

界面跟随游戏语言：English、简体中文、Deutsch、한국어、Português (Brasil)、Español (Latinoamérica)、Français、日本語、Italiano、Русский、Українська。玩家输入的名字保持原样；部分新增提示、日志和贴图文字可能保留英文或原语言。

The interface follows the game language in the 11 languages above. Player-entered names are preserved; some newer prompts, diagnostics and lettering embedded in artwork may retain their original language.

下载后可用 PowerShell 计算校验值，与同名 `.sha256` 附件比较：

```powershell
Get-FileHash -Algorithm SHA256 -LiteralPath './CyclopsRestored-v0.9.0-beta.2-Win64.zip'
Get-FileHash -Algorithm SHA256 -LiteralPath './CyclopsRestored-v0.9.0-beta.2-Source.zip'
```

本版沿用已核验的 beta.13 安装文件：98 个 Lua 文件、原生供电桥与含 778 个资源的内容包。源码附件包含相同的运行脚本、原生桥与编辑器工具的自编代码；不包含游戏原始资源、SDK、引擎、存档或私有日志。离线测试、编辑器核验和文件校验不等同于完整实机验收。

The release preserves the verified beta.13 payload: 98 Lua files, the native power bridge and cooked content containing 778 assets. The source attachment includes matching runtime scripts and original native/editor code. Game source assets, SDKs, engine files, saves and private logs are excluded; a source checkout alone cannot rebuild the art package. Offline/editor/package checks do not establish complete gameplay acceptance.

免费、非官方同人 Mod，非 Unknown Worlds / KRAFTON 官方作品。MIT 授权仅覆盖自编代码、文档与翻译，不覆盖原游戏资产或第三方软件。

Free, unofficial fan mod, not endorsed by Unknown Worlds or KRAFTON. The MIT license covers original code, documentation and translations, not original game assets or separately licensed dependencies.
