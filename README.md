# Cyclops Restored / 独眼巨人号

Unofficial Cyclops mobile-base submarine mod for Subnautica 2.

**[下载与完整发布说明 / Downloads and release notes](https://github.com/raevenkelby6674-byte/SN2-CyclopsRestored/releases/tag/v0.9.0-beta.1)**

## 已知问题 / Known issues

- **柜子重命名暂时有显示 bug。Locker renaming still has a display bug.**
- **自定义外观暂时也有显示 bug。Custom appearance still has a display bug.**

这两项尚未修复，本版不宣称显示效果全部还原。船壳不显示船名是当前设定，名称用于信标。
These display issues remain open in this beta. Ship names intentionally appear on the beacon, not the hull.

## 版本与下载 / Compatibility and downloads

**Windows Steam · 单人模式 / single-player · Subnautica 2 0.1.2.3-131439**

安装包、源码包及两个 SHA-256 校验文件见上方发布页的附件区。完整安装方法如下；上游加载器单独安装。
The install ZIP, source bundle and both checksum files are on the release page linked above. Install the loader separately and follow the steps below.

## 安装步骤 / Installation

**前置条件：Windows Steam 单人模式，游戏版本 `0.1.2.3-131439`。完全退出游戏后操作，先备份存档。**

1. **找到游戏根目录。** Steam 库 → 右键 Subnautica 2 → 管理 → 浏览本地文件。这里能看到 `Subnautica2.exe` 和 `Subnautica2` 文件夹。
2. **安装 UE4SS 加载器。** 使用支持游戏所用 UE 5.6 的 Windows x64 构建。本版开发测试使用 `v3.0.1 Beta #0`、提交 `1ba38db4`（压缩包版本 `3.0.1-1176-g1ba38db4`）；其他构建尚未验证。[上游下载页](https://github.com/UE4SS-RE/RE-UE4SS/releases/tag/experimental-latest) · [安装文档](https://docs.ue4ss.com/dev/installation-guide.html)。将加载器包中的 `dwmapi.dll` 和 `ue4ss` 文件夹放到 `<游戏根目录>/Subnautica2/Binaries/Win64/`，与 `Subnautica2-Win64-Shipping.exe` 同级。已有兼容加载器的玩家可跳过这一步。原 Subnautica 2 专用分支已归档并指向上游。
3. **安装本 Mod。** 下载附件 `CyclopsRestored-v0.9.0-beta.1-Win64.zip`，将其中的 `Subnautica2` 文件夹复制到第 1 步的游戏根目录并合并。Mod 安装包的解压位置是游戏根目录；不要把整个 Mod 包放进 `Win64` 或再套一层版本号文件夹。
4. **核对目录。** 安装后应包含下面列出的文件；内容插件和 Lua 脚本两部分都需要。
5. **启动并使用。** 从 Steam 正常启动游戏并进入单人存档。界面语言跟随游戏设置。使用栖息所建造器放置“海面载具建造平台”，移到开阔深水区后使用平台屏幕制造独眼。

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

**更新：** 完全退出游戏，备份旧版后，仅替换上述两个 `CyclopsRestored` 文件夹。保留存档、UE4SS 和其他 Mod。

**未生效时：** 先核对游戏版本和上面的两条 Mod 路径，再查看 `Subnautica2/Binaries/Win64/ue4ss/UE4SS.log`。原生供电桥有版本校验，游戏更新后不要强制绕过。

**English:**

1. In Steam, right-click Subnautica 2 → Manage → Browse local files. This opens the game root containing `Subnautica2.exe` and the `Subnautica2` folder. Exit the game and back up your save.
2. Install a Windows x64 UE4SS build compatible with UE 5.6. The tested build is `v3.0.1 Beta #0 / 1ba38db4` (`3.0.1-1176-g1ba38db4`); other builds are not validated. Use the upstream links above. Place the loader’s `dwmapi.dll` and `ue4ss` folder in `<game root>/Subnautica2/Binaries/Win64/`, next to the shipping executable. Skip this if a compatible loader is already installed.
3. Download **`CyclopsRestored-v0.9.0-beta.1-Win64.zip`**. Merge its `Subnautica2` folder into the **game root**, preserving the structure shown above. Both the content plugin and Lua/native runtime are required. `Source.zip` and GitHub’s automatically generated source archives are not install packages.
4. Start through Steam in single-player. The UI follows the game language. Place a Mobile Vehicle Bay with the Habitat Builder and use its screen in deep, open water to construct the Cyclops.
5. To update, exit the game, back up the old mod and replace only the two `CyclopsRestored` folders. Keep saves, UE4SS and other mods. If loading fails, check the directory layout, supported game build and `ue4ss/UE4SS.log`. Do not bypass the native version checks.

**校验 / Checksums** — the two `.sha256` attachments contain the expected ZIP hashes. PowerShell:

```powershell
Get-FileHash -Algorithm SHA256 -LiteralPath './CyclopsRestored-v0.9.0-beta.1-Win64.zip'
Get-FileHash -Algorithm SHA256 -LiteralPath './CyclopsRestored-v0.9.0-beta.1-Source.zip'
```

## 多语言 / Languages

界面跟随游戏语言，保留玩家输入的柜名、船名。
The interface follows the game language and preserves player-entered names.

English · 简体中文 · Deutsch · 한국어 · Português (Brasil) · Español (Latinoamérica) · Français · 日本語 · Italiano · Русский · Українська

169 条文本，11 种语言；原生文本注册、资源重载、按钮尺寸适配和数量弹窗已核验。诊断日志和模型贴图内文字可能保留原语言。
169 text entries in 11 languages, with native text registration, resource reload and quantity-picker layout checks. Diagnostic logs and lettering embedded in artwork may retain their original language.

## 验证 / Validation

1,859 translation values, 4,510 serialized field checks, 11 native Slate renders, 12 behavioral regression suites, 70 Lua modules compiled, and 536 cooked assets checked. These are offline/editor/package checks, not exhaustive gameplay acceptance in every language. The power DLL and existing power rules are unchanged from the preceding installed candidate.

Win64 ZIP SHA-256: `34db95ade73ca0faeba05836499a5ca0e2c4e7dfdfa152404c85df7f7527ae79`

免费、非官方同人 Mod，非 Unknown Worlds / KRAFTON 官方作品。代码的 MIT 授权不覆盖原游戏资产或第三方软件。
Unofficial free fan mod, not endorsed by Unknown Worlds or KRAFTON. The MIT code license does not cover original game assets or third-party software.

## 源码 / Source

完整自编代码和翻译在发布附件 **CyclopsRestored-v0.9.0-beta.1-Source.zip** 中，共 121 个源码与说明文件，并附代码许可证。GitHub 自动生成的 Source code 压缩包仅包含仓库当前文件；本测试版的完整代码请使用明确命名的 Source.zip 附件。

The complete original mod code and translations are provided in the explicitly named **CyclopsRestored-v0.9.0-beta.1-Source.zip** release attachment, with 121 source/documentation files and the code license. GitHub’s automatically generated source archives contain the repository files only.
