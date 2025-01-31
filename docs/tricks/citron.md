# <img src="/assets/emulators/citron.png" alt="EmuDeck guide" width="80" style="vertical-align: middle"> Citron Tips and Tricks

[TOC]

---

### How to Configure Gyro

[Back to the Top](#citron-table-of-contents)

Gyro for Citron requires SteamDeckGyroDSU. SteamDeckGyroDSU can be installed via EmuDeck, or it can be installed manually.

Visit [SteamDeckGyroDSU](../../emudeck-application/steamos/emudeck-application-101.md#steamdeckgyrodsu) to learn how to install and utilize SteamDeckGyroDSU.

#### How to Diagnose Gyro

Gyro with Citron on the Steam Deck can be a little finnicky. Prior to following the steps below, make sure you have already tried resetting Citron's configurations to EmuDeck's defaults in the EmuDeck application.
If that still does not resolve the issue, you can take a look in the Citron settings and try to to set the gyro controls yourself.

**Here's How**

1. Add Citron to Steam so you may open it in Game Mode
   - You may add Citron to Steam by using the `Emulators` parser in Steam ROM Manager
2. Install and configure gyro for the Citron shortcut in Game Mode
   - Read the instructions on the [SteamDeckGyroDSU](../../emudeck-application/steamos/emudeck-application-101.md#steamdeckgyrodsu) page to learn how to install and utilize SteamDeckGyroDSU in Game Mode
3. In Game Mode, on the Citron shortcut, click the `Gear` icon
4. Select `Properties`
5. Scroll down to `Game Resolution`
6. Change it to `3840x2160`
7. Enable `Set resolution for internal and external display`
8. In Game Mode, open Citron
9. Click `Emulation` at the top, click `Configure`
10. Click `Controls` on the left
11. Make sure the `emudeck` profile is selected in the `Profile` drop-down menu in the top right
12. Under `Motion 1` at the bottom, click `[Not Set]` or `sdl` and shake your Steam Deck
13. Click `OK` in the bottom right
14. Exit out of Citron
15. In Game Mode, on the Citron shortcut, click the `Gear` icon
16. Select `Properties`
17. Scroll down to `Game Resolution`
18. Change it to `Default`
19. Disable `Set resolution for internal and external display`
20. Test gyro on a Nintendo Switch game using Citron in Game Mode
    - You may do so by opening the game through Citron directly, adding the game as a shortcut through Steam ROM Manager, or opening the game through ES-DE

---

### How to Configure Gyro With External Controllers

[Back to the Top](#citron-table-of-contents)

#### Desktop Mode

1. Switch to Desktop Mode
2. Exit out of Steam
   - You may exit out of Steam a couple of different ways:
     - Right click the `Steam` icon in your taskbar and click `Exit Steam`
     - Open Steam, click the `Steam` button in the top left, click `Exit`
     - Open a terminal (Konsole) and enter `killall -9 steam`
     - Do note that clicking the the `X` button in the top right of the Steam window **will not** exit out of Steam
   - Your controls will switch to `Lizard Mode`. Use `L2` to right click, `R2` to left click, and the `Right Trackpad` to move the mouse
   - You may also connect an external keyboard and mouse
3. Click the bluetooth icon in the bottom right of your taskbar and connect your controller
   - <img src="https://github.com/dragoonDorise/EmuDeck/assets/108900299/24945d4c-df06-4fbe-9668-7becea0c5edb" height="300">
4. Right click anywhere on the blank space on your desktop and click `Configure Display Settings`
   - You may also find this menu by opening `System Settings` and clicking `Display and Monitor`
5. Click the `Upside Down` configuration under `Orientation`
   - This setting will switch your Steam Deck to "Portrait Mode", hold your Steam Deck sideways for this section to navigate the various settings
6. Open Citron
7. Click `Emulation` at the top, click `Configure`
8. Click `Controls` on the left
9. Under `Input Device`, select your external controller
10. Under `Motion 1` at the bottom, click `[Not Set]` or `sdl` and shake your controller
11. (Optional), you may also choose to save your layout as a unique profile. With this profile, you can choose to apply it on a per-game basis
12. Click `OK` in the bottom right
13. Exit out of Citron
14. Right click anywhere on the blank space on your desktop and click `Configure Display Settings`
    - You may also find this menu by opening `System Settings` and clicking `Display and Monitor`
15. Click the `90 Counterclockwise` configuration under `Orientation`
16. Switch to `Game Mode`

#### Game Mode

1. In Game Mode, connect your controller
2. Select your Nintendo Switch game
3. On the `Play` screen, select the `Controller` icon to the right of the screen
   - <img src="https://github.com/dragoonDorise/EmuDeck/assets/108900299/468d63e3-534c-4270-ac61-06e167d6df48" height="300">
4. Select your controller tab at the top
   - <img src="https://github.com/dragoonDorise/EmuDeck/assets/108900299/b51a1405-9cdf-4ba3-bebf-db817f057f63" height="300">
5. Click the `Gear` icon to the right, and click `Disable Steam Input`
   - <img src="https://github.com/dragoonDorise/EmuDeck/assets/108900299/33cbcb8e-a444-4a75-8e4a-ba9451e6e07a" height="300">
   - You may need to restart first for this setting to properly apply
6. Your controller's gyro will now work for this selected game, repeat as needed for your other games

If your controller gyro does not work after the above steps, reset Citron's configuration in the EmuDeck application on the Manage Emulators page and try again.

#### Post-Configuration

To restore the default Steam Deck controls:

1. Open Citron
2. Click `Emulation` at the top, click `Configure`
3. Click `Controls` on the left
4. Under the `Profile` drop-down menu in the top right, select `emudeck`
   - The EmuDeck configured controls should now auto-populate
5. Select `Steam Virtual Gamepad 0` under `Input Device`
6. Click `OK` in the bottom right
7. Exit out of Citron

(Optional) To restore Steam Input:

1. Select your Nintendo Switch game
2. On the `Play` screen, select the `Controller` icon to the right of the screen
   - <img src="https://github.com/dragoonDorise/EmuDeck/assets/108900299/468d63e3-534c-4270-ac61-06e167d6df48" height="300">
3. Select your controller tab at the top
   - <img src="https://github.com/dragoonDorise/EmuDeck/assets/108900299/b51a1405-9cdf-4ba3-bebf-db817f057f63" height="300">
4. Click the `Gear` icon to the right, and click `Enable Steam Input`
   - You may need to restart first for this setting to properly apply
5. The controls will be reverted to Steam Input and the Steam Deck controls will be restored

---

### How to Optimize Performance (Power Tools)

[Back to the Top](#citron-table-of-contents)

Visit [Power Tools](../../emudeck-application/steamos/emudeck-application-101.md#power-tools) to learn how to optimize performance using Power Tools.

---

### How to Configure Multiplayer

[Back to the Top](#citron-table-of-contents)

Multiplayer for Citron is configured out of the box, no additional configuration is needed.

You may need to re-arrange the controller order in Game Mode for your controllers to function as expected. See [How to Re-Arrange the Controller Order](../../controls-and-hotkeys/steamos/external-controllers.md#how-to-re-arrange-the-controller-order) for more information.

---

### How to Install Mods

[Back to the Top](#citron-table-of-contents)

**Mod Resources**

_This list is not comprehensive_

- Citron Mods: [https://citron-emu.org/wiki/switch-mods/](https://citron-emu.org/wiki/switch-mods/)
  - This is not an exhaustive list of mods available for Citron
  - Alternate link: https://github.com/citron-emu/citron/wiki/Switch-Mods
- Citron Mod Instructions: [https://citron-emu.org/help/feature/game-modding/](https://citron-emu.org/help/feature/game-modding/)
- GameBanana Mods: [https://gamebanana.com/](https://gamebanana.com/)
  - Search by game name
- Nexus Mods: [https://www.nexusmods.com/](https://www.nexusmods.com/)
  - Search by game name
- GBAtemp: [https://gbatemp.net/forums/nintendo-switch.283/?prefix_id=56](https://gbatemp.net/forums/nintendo-switch.283/?prefix_id=56)
  - Use [https://gbatemp.net/search/?type=post](https://gbatemp.net/search/?type=post) to search
    - Sort by `ROM Hack` in the prefixes list and `Nintendo Switch` in the `Search in forums` list
  - To narrow search results, use the `Search titles only` toggle
- SweetFX: [http://sfx.thelazy.net/games/](http://sfx.thelazy.net/games/)
  - Search by game name
- theboy181
  - 1: Github Collection: [https://github.com/theboy181/switch-ptchtxt-mods](https://github.com/theboy181/switch-ptchtxt-mods)
  - 2: Github Collection: [https://github.com/theboy181/switch-cheat-mods](https://github.com/theboy181/switch-cheat-mods)
  - 3: theboy181's Discord: [https://linktr.ee/theboy181](https://linktr.ee/theboy181)

---

**Preface**

For Citron's instructions on how to install mods, see: [https://citron-emu.org/help/feature/game-modding/](https://citron-emu.org/help/feature/game-modding/)

The **folder structure** of a mod **is important**. It should generally look like the following:

```
mod_directory
  - exefs
  - romfs
  - romfs_ext
```

A few examples:

```
# Blur Removal Mod for The Legend of Zelda: Link's Awakening

Blur Removal
  - exefs
      - Zelda-Links Awakening v1.0.1 - DOF.pchtxt
```

```
# 60 FPS Mod for The Legend of Zelda: Link's Awakening

Stable-60fps-v2
  - exefs
      - 1.0.0.pchtxt
```

```
# Faster Battles Mod for Pokemon Brilliant Diamond

Faster Battles
  - romfs
      - Data
         - StreamingAssets
             - AssetAssistant
                 - Battle
                     - battle_masterdatas
```

---

**Tutorial**

1. In Desktop Mode, open Citron
2. Right click a game you intend on modding
3. Click `Open Mod Data Location`
   1. Visual Reference: <img src="https://user-images.githubusercontent.com/108900299/201798674-bdc115fd-b6f9-465f-a9d3-39374e756a97.png" height="300">
4. Place your mod folder in the opened folder
   1. You may need to extract the mod first
   2. Visual Reference: <img src="https://user-images.githubusercontent.com/108900299/201798900-ec578de7-de6f-45f7-b5a4-dfc2fd82b4c3.png" height="300">
5. In Citron, right click the same game, open `Properties`, click the `Add-Ons` tab
6. Check the box to the left of your mod(s)
   1. Visual Reference: <img src="https://user-images.githubusercontent.com/108900299/201799059-bd2e8a1a-0549-47ea-9d7b-1b5b75807f8d.png" height="300">
7. Your mod is now installed

---

### Special Game Configurations

[Back to the Top](#citron-table-of-contents)

Some games will take additional setup, requiring mods or an extensive alteration of settings. The EmuDeck Community Creations page collects these configurations in one centralized location.

To submit or view special game configurations, see [Special Game Configurations](../../community-creations/steamos/community-game-configurations.md#citron-nintendo-switch).

**Current List of Special Game Configurations**

- The Legend of Zelda: Link's Awakening

---

### How to Set Up Early Access

[Back to the Top](#citron-table-of-contents)

EmuDeck 2.1 added an option to enable Citron (Early Access).

**Here's how to set it up**

1. Open EmuDeck
2. Click the `Manage Emulators` button
3. Click `Citron`
4. Click `Setup Early Access`
5. Enter your token
6. Whenever you launch Citron, it will now use the `Early Access` version

---

### How to Roll Back Citron to an Older Version

[Back to the Top](#citron-table-of-contents)

#### Preface

Your ROMs launch using a script created by EmuDeck, `citron.sh` in `Emulation/tools/launchers`.

The script launches the corresponding emulator in `/home/deck/Applications` and **specifically looks** for two traits:

- The most recently downloaded version of the emulator in `/home/deck/Applications`, based on the file/release date.
- The emulator name at the beginning of the file. Anything after the emulator name is ignored.
  - For example, if the latest version of the emulator is `1351` and you would like to downgrade to `1349`. When you download version `1349`, you could rename it to `EMULATORNAME-1349.AppImage`, and EmuDeck's script will ignore the `-1349` in the file name, allowing you to record which versions of the emulator you are using through the file name.

#### How to Roll Back Citron

1. Download the version of the emulator you would like to use from Citron's GitHub: [https://github.com/citron-emu/citron-mainline/releases](https://github.com/citron-emu/citron-mainline/releases)
2. Move the downloaded emulator from Step 1 to `/home/deck/Applications`
3. (Optional) Rename or delete the original emulator file
4. Right click the newly downloaded emulator, click `Properties`, click `Permissions`, check `Is executable`
5. Your games will now launch using the version of the emulator you downloaded

---

### How to Select Between Citron and Ryujinx in Game Mode

[Back to the Top](#citron-table-of-contents)

If you are using Steam ROM Manager and would like to run some games through Citron and others through Ryujinx, you may use Steam ROM Manager's exception manager to selectively run your games in your preferred emulator.

For further instructions, see [Steam ROM Manager: How to Hide ROMs on a Per Parser Basis](../../tools/steamos/steam-rom-manager.md#how-to-hide-roms-on-a-per-parser-basis).

If you are using ES-DE, you may use ES-DE's alternative emulators feature to select on a per-game basis which to run through Citron and which to run through Ryujinx.

For further instructions, see [ES-DE: How to Select a Different Emulator on a Per-Game Basis](../../tools/steamos/es-de.md#how-to-select-a-different-emulator-on-a-per-game-basis).

---

### How to Configure Language Settings

[Back to the Top](#citron-table-of-contents)

#### UI

1. In Desktop Mode, open Citron
2. At the top, click `Emulation`, click `Configure`
3. On the left, click the `General` tab
4. Click the `UI` tab
5. To the right of `Interface Language`, select your preferred language in the drop-down menu

#### In-Game

1. In Desktop Mode, open Citron
2. At the top, click `Emulation`, click `Configure`
3. On the left, click the `System` tab
4. Click the `System` tab
5. To the right of `Language`, select your preferred language in the drop-down menu

---
