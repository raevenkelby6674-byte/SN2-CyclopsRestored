<h1 align="center">Cyclops Restored</h1>

<p align="center"><strong>The Cyclops submarine for Subnautica 2</strong></p>

<p align="center">Bring the original Cyclops into Subnautica 2 as a mobile base you can pilot, build inside and dock your Tadpole in.</p>

<p align="center"><strong>English</strong> | <a href="./README.zh-CN.md">中文</a></p>

<p align="center">
  <a href="https://github.com/raevenkelby6674-byte/SN2-CyclopsRestored/releases/tag/v0.9.0-beta.3">Download</a> ·
  <a href="#download-and-installation">Installation</a> ·
  <a href="#features">Features</a> ·
  <a href="#whats-new">What's new</a> ·
  <a href="https://github.com/raevenkelby6674-byte/SN2-CyclopsRestored/releases/download/v0.9.0-beta.3/CyclopsRestored-Source.zip">Source</a> ·
  <a href="https://github.com/raevenkelby6674-byte/SN2-CyclopsRestored/issues">Feedback</a>
</p>

## Features

- **Piloting and exploration:** speed settings, engine efficiency upgrades, interior and exterior lights, external cameras, sonar, shields and decoys.
- **Interior building:** place native game facilities inside the ship and connect them to its power network. Supports onboard generators and Tadpole docking, charging and repairs.
- **Storage and upgrades:** keeps the original locker layout. The three storage compression tiers allow stacks of **32 / 64 / 128** matching items. Middle-click to choose how many items to take. Tools and batteries with individual data remain separate.
- **Deep diving:** starts at a crush depth of **1,000 m**. The three depth upgrades raise it to **3,000 / 6,000 / 10,000 m**.
- **Names and colors:** locker names appear on their original nameplates, while the ship name appears on its beacon. The color editor includes a rotatable 3D preview.
- **Wreck recovery:** when hull health reaches zero, the ship leaves a wreck with recoverable supplies and modules. Each occupied locker slot is packed into one cargo sphere, preserving the item count and data.
- **Co-op:** every player can pilot, use storage, install modules and build inside the ship. The helm still follows normal seat occupancy rules.

A cargo sphere makes one unpack attempt when placed in an intact Cyclops locker. Capacity follows that ship's current storage upgrade. If there is not enough room, the sphere stays intact; free up space and reinsert it to try again.

## Download and installation

**For Subnautica 2 on Windows Steam, game build `0.1.2.3-131439`.** The matching loader is UE4SS `v3.0.1 Beta #0` (`1ba38db4`, package `3.0.1-1176-g1ba38db4`). This mod is for the sequel, not the first Subnautica or Below Zero.

To play, download **`CyclopsRestored-Win64.zip`**. `CyclopsRestored-Source.zip` contains development source, not an installable mod. These filenames will stay the same across updates; the actual build is recorded in `VERSION.txt` inside the archive.

1. Fully exit the game.
2. Install the matching UE4SS build. Place its `dwmapi.dll` and `ue4ss` folder in `Subnautica2/Binaries/Win64/`, beside `Subnautica2-Win64-Shipping.exe`. Skip this step if that version is already installed. [UE4SS downloads](https://github.com/UE4SS-RE/RE-UE4SS/releases/tag/experimental-latest) · [Installation guide](https://docs.ue4ss.com/dev/installation-guide.html)
3. Extract the Win64 archive and **merge its `Subnautica2` folder into the game root**. In Steam, choose **Manage → Browse local files** to find that folder.
4. Start the game. For co-op, the host and every joining player need the same complete mod package.

The installation should contain these two folders:

```text
Game root/
└─ Subnautica2/
   ├─ Mods/CyclopsRestored/
   │  ├─ CyclopsRestored.uplugin
   │  └─ Content/Paks/Windows/   (.pak, .utoc, .ucas)
   └─ Binaries/Win64/ue4ss/Mods/CyclopsRestored/
      ├─ enabled.txt
      ├─ Scripts/
      └─ native/CyclopsFinitePower.dll
```

**Updating an older version:** exit the game, move the two `CyclopsRestored` folders shown above outside the game directory, then install the new files. This keeps old scripts from being mixed with the update. Keep your saves, UE4SS and other mods.

## Building the Cyclops in game

Use the Habitat Builder to place the Mobile Vehicle Bay. In sufficiently deep, open water, use the bay's control screen to build the Cyclops. Once aboard, use the native Habitat Builder to place interior facilities and the ship's upgrade station to install modules.

The interface follows the game language, with 11 languages including Chinese, English, Japanese and Korean.

## What's new

The third public beta focuses on multiplayer interactions, docking, cargo recovery and power updates:

- Adds missing hatch models, helm prompts and several interior interactions for joining players, and adjusts hatch closure after docking.
- Fixes input not being returned after leaving the helm or closing customization, and clears editing state left behind by an invalid ship.
- Improves synchronization when players use storage, modules or customization together, and fixes locker names not being saved.
- Fixes interrupted cargo recovery so that later recovery operations do not interfere with one another.
- Fixes power updates for interior facilities and generator modules, and reduces repeated power reads when players take turns interacting.

This release uses internal build `0.9.0-beta.23-mp-test`. Code and offline checks are complete; feedback from longer co-op sessions and in-game performance testing is still being collected.

## Source and feedback

The source archive includes the project's Lua code, native bridge, editor tools, translations and tests under the MIT license. See `BUILDING.md` inside the archive for development instructions. Licenses and asset notices are included there as well.

To report a bug, open an Issue with your game and mod versions, whether you were hosting or joining, and the steps that triggered it. A screenshot or relevant log excerpt helps.
