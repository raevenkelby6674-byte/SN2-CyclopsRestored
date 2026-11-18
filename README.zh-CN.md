<h1 align="center">Cyclops Restored</h1>

<p align="center"><strong>《Subnautica 2：异星水域》独眼巨人号 Mod</strong></p>

<p align="center">把一代的独眼巨人号带到二代，作为能驾驶、能停靠小艇、也能布置内部设施的移动基地。</p>

<p align="center"><a href="./README.md">English</a> | <strong>中文</strong></p>

<p align="center">
  <a href="https://github.com/raevenkelby6674-byte/SN2-CyclopsRestored/releases/tag/v0.9.0-beta.5">下载</a> ·
  <a href="#下载与安装">安装</a> ·
  <a href="#能做什么">功能</a> ·
  <a href="#这次更新">更新内容</a> ·
  <a href="https://github.com/raevenkelby6674-byte/SN2-CyclopsRestored/releases/download/v0.9.0-beta.5/CyclopsRestored-Source.zip">源码</a> ·
  <a href="https://github.com/raevenkelby6674-byte/SN2-CyclopsRestored/issues">反馈</a>
</p>

## 能做什么

- **还原装备**：凝滞枪使用一代模型、动画、蓄力效果和音效，接入二代物品栏、电池及制作流程。同款测试枪两次有效命中即可摧毁满血独眼。
- **开船与探索**：档位切换、引擎效率升级、内外照明、外部摄像头、声呐、护盾和诱饵。
- **布置船舱**：在船内建造原版设施，共用独眼电网；支持舱内发电机和蝌蚪号停靠、充电、维修。
- **储物与升级**：保留原来的柜子布局。三级储物压缩模块的同类物品堆叠上限分别为 **32 / 64 / 128**，中键可选择取出数量。带独立数据的工具和电池单独存放。
- **深潜**：初始耐压深度 **1000 米**，三级深度模块分别提升到 **3000 / 6000 / 10000 米**。
- **命名与配色**：柜名显示在原铭牌上；船名用于信标。外观编辑带可旋转的 3D 预览。
- **残骸回收**：生命值清零后留下残骸，物资和模块可以回收。柜子每个占用格的物资会保存为一个压缩球，保留数量与物品数据。
- **多人游玩**：所有玩家都可以使用驾驶、储物、模块、建造等功能，驾驶位按正常占用规则使用。

压缩球放入完好独眼的储物柜后尝试还原一次，容量按接收船的储物模块等级计算。空间不足时保留原球，腾出空间后重新放入即可。

## 下载与安装

**适用：Subnautica 2，Windows Steam，游戏版本 `0.1.2.3-131439`。** 配套加载器为 UE4SS `v3.0.1 Beta #0`（`1ba38db4`，包版本 `3.0.1-1176-g1ba38db4`）。这是二代 Mod，一代和 Below Zero 不能使用。

玩家只需下载 **`CyclopsRestored-Win64.zip`**。`CyclopsRestored-Source.zip` 是开发源码，不是安装包。文件名以后保持不变，实际版本记录在包内 `VERSION.txt`。

1. 完全退出游戏。
2. 安装配套 UE4SS，将加载器的 `dwmapi.dll` 和 `ue4ss` 文件夹放到 `Subnautica2/Binaries/Win64/`，与游戏的 `Subnautica2-Win64-Shipping.exe` 同级。已有上述版本可跳过。[UE4SS 下载](https://github.com/UE4SS-RE/RE-UE4SS/releases/download/experimental/UE4SS_v3.0.1-1176-g1ba38db4.zip) · [安装说明](https://docs.ue4ss.com/dev/installation-guide.html)
3. 解压 Win64 包，把里面的 **`Subnautica2` 文件夹合并到游戏根目录**。Steam 中可通过“管理 → 浏览本地文件”找到根目录。
4. 启动游戏。联机时，主机和每位加入者都安装同一份完整包。

安装后应有这两个目录：

```text
游戏根目录/
└─ Subnautica2/
   ├─ Mods/CyclopsRestored/
   │  ├─ CyclopsRestored.uplugin
   │  └─ Content/Paks/Windows/   (.pak、.utoc、.ucas)
   └─ Binaries/Win64/ue4ss/Mods/CyclopsRestored/
      ├─ enabled.txt
      ├─ Scripts/
      └─ native/CyclopsFinitePower.dll
```

**从旧版更新：** 退出游戏后，先把上面两个 `CyclopsRestored` 文件夹移到游戏目录外，再放入新包里的文件，避免旧脚本残留。保留存档、UE4SS 和其他 Mod。

## 在游戏里建造

使用建造器放置“海面载具建造平台”，在水深足够、周围开阔的位置，通过平台操作屏制造独眼。进入船舱后可使用原版建造器布置设施；升级模块在船内模块站安装。

界面会跟随游戏语言，提供中文、英文、日文、韩文等 11 种语言。

## 这次更新

独眼的干舱现在单独渲染。透过舷窗仍能看到海水，底部停靠井保持进水。原版基地接入了同一套隔水处理。联机时每个人按自己的镜头独立显示，舱内画面的宽高各取当前视图的一半。

凝滞枪和测试枪接回了游戏的装备、收起和卸下流程。凝滞枪现在能读取命中目标，展开力场。修正了新船关闭推力时垂直速度上限也变成零的问题。已经下水的船会停止查询水面。

内部版本为 `0.9.0-beta.27-restoration-test`，联机协议 4。船舱和持枪模型已在编辑器中检查，存档内的实际表现、双机联机与帧率仍待测试。储物柜铭牌和自定义外观界面偶尔会显示异常。

## 开源与反馈

源码包包含本项目的 Lua、原生桥、编辑器工具、翻译和测试，按 MIT 许可开放。开发方法见包内 `BUILDING.md`，资源说明和许可证也放在包内。

发现问题可以提 Issue，写上游戏和 Mod 版本、主机或加入者、触发步骤，附上截图或相关日志即可。
