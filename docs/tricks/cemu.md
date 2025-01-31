# <img src="/assets/emulators/cemu.png" alt="EmuDeck guide" width="80" style="vertical-align: middle"> Cemu Tips and Tricks

[TOC]

### How to Configure Gyro

Gyro for Cemu requires SteamDeckGyroDSU. SteamDeckGyroDSU can be installed via EmuDeck, or it can be installed manually.

Gyro only works with the Wii U Gamepad (enabled by default). If you changed your controller layout to the Pro Controller, gyro will not work.

Read [How to Use the Wii U Pro Controller Configuration](#how-to-use-the-wii-u-pro-controller-configuration) to learn how to apply the Pro Controller layout on a per game basis.

Visit [SteamDeckGyroDSU](../../../emudeck-application/steamos/emudeck-application-101.md#steamdeckgyrodsu) to learn how to install and utilize SteamDeckGyroDSU.

---

### How to Configure Gyro With External Controllers

Some external controllers, including the Sony DualSense and the Nintendo Switch Pro Controller feature gyro controls. Cemu allows you to use this gyro with a little bit of set up.

**Here's How**

#### Desktop Mode

1. Switch to Desktop Mode
2. Exit out of Steam
   - You may exit out of Steam a couple of different ways:
     - Right click the `Steam` icon in your taskbar and click `Exit Steam`
     - Open Steam, click the `Steam` button in the top left, click `Exit`
     - Open a terminal (Konsole) and enter `killall -9 steam`
     - Do note that clicking the the `X` button in the top right of the Steam window **will not** exit out of Steam
   - Your controls will switch to `Lizard Mode`. Use `L2` to right click, `R2` to left click, and the `Right Trackpad` to move the mouse
3. Click the bluetooth icon in the bottom right of your taskbar and connect your controller
   <img src="https://github.com/dragoonDorise/EmuDeck/assets/108900299/24945d4c-df06-4fbe-9668-7becea0c5edb" height="300">
4. Click the Steam icon in the bottom left of the taskbar and open `Cemu AppImage`
   <img src="https://github.com/dragoonDorise/EmuDeck/assets/108900299/e395d988-cf13-4b2c-af2c-e27059b44ac2" height="300">
5. At the top of the Cemu GUI, click `Options`, click `Input settings`
6. Under the `Controller 1` tab, press the `-` button to the right of the `Controller` drop-down twice
   <img src="https://github.com/dragoonDorise/EmuDeck/assets/108900299/d2b7eb25-e5a2-4140-9c8e-069e5c465ab5" height="300">
7. The drop-down box will be empty and your controls will no longer be mapped, this is expected behavior
   <img src="https://github.com/dragoonDorise/EmuDeck/assets/108900299/c38668d2-a128-415a-b4fa-756e4e254c53" height="300">
8. Under the `Controller 1` tab, press the `+` button to the right of the `Controller` drop-down
   <img src="https://github.com/dragoonDorise/EmuDeck/assets/108900299/3f0e4a6b-5355-420f-9def-5423cc1c0116" height="300">
9. Select `SDLController` for the `API` drop-down and select your controller under the `Controller` drop-down
   <img src="https://github.com/dragoonDorise/EmuDeck/assets/108900299/10c359ca-0737-4c47-bbd9-c095777cfd42" height="300">
10. Click the `Add` button and Cemu will auto-map your controls
11. Click the `Settings` button under the drop-down with your controller name
12. Check the box to the left of `Use motion`
    <img src="https://github.com/dragoonDorise/EmuDeck/assets/108900299/388f1867-dd5d-4eb1-bd9f-d0fbf39896d8" height="300">
13. Click the `OK` button
14. Give the profile a unique name under the `Profile` drop-down box at the top and click `Save`
    <img src="https://github.com/dragoonDorise/EmuDeck/assets/108900299/5c64751c-041f-40a5-86a5-bc8c6615eb58" height="300">
15. Your controller is now configured with gyro, proceed to the `Game Mode` section to start using your controller in `Game Mode`

#### Game Mode

1. In Game Mode, connect your controller
2. Select your Wii U game
3. On the `Play` screen, select the `Controller` icon to the right of the screen
   <img src="https://github.com/dragoonDorise/EmuDeck/assets/108900299/468d63e3-534c-4270-ac61-06e167d6df48" height="300">
4. Select your controller tab at the top
   <img src="https://github.com/dragoonDorise/EmuDeck/assets/108900299/b51a1405-9cdf-4ba3-bebf-db817f057f63" height="300">
5. Click the `Gear` icon to the right, and click `Disable Steam Input`
   <img src="https://github.com/dragoonDorise/EmuDeck/assets/108900299/33cbcb8e-a444-4a75-8e4a-ba9451e6e07a" height="300">
   - You may need to restart first for this setting to properly apply
6. Your controller's gyro will now work for this selected game, repeat as needed for your other games

#### Post-Configuration

This section went over creating a new Player 1 profile for your external controller.

To switch between your new controller profile and the Steam Deck controller profile, open Cemu and open the input settings, select your preferred option in the `Profile` drop-down menu and click `Load`.

To switch back to the Steam Deck controls, select the `Deck-Gamepad-Gyro` profile:

<img src="https://github-production-user-asset-6210df.s3.amazonaws.com/108900299/242173410-54e3d6fb-a38b-499e-ba1a-f65e809ef439.png" height="300">

(Optional) To restore Steam Input:

1. Select your Nintendo Wii U game
2. On the `Play` screen, select the `Controller` icon to the right of the screen
   <img src="https://github.com/dragoonDorise/EmuDeck/assets/108900299/468d63e3-534c-4270-ac61-06e167d6df48" height="300">
3. Select your controller tab at the top
   <img src="https://github.com/dragoonDorise/EmuDeck/assets/108900299/b51a1405-9cdf-4ba3-bebf-db817f057f63" height="300">
4. Click the `Gear` icon to the right, and click `Enable Steam Input`
   - You may need to restart first for this setting to properly apply
5. The controls will be reverted to Steam Input and the Steam Deck controls will be restored

---

### How to Optimize Performance (Power Tools)

Visit [Power Tools](../../../emudeck-application/steamos/emudeck-application-101.md#power-tools) to learn how to optimize performance using Power Tools.

---

### How to Configure Multiplayer

1. Open Cemu
2. It's recommended you enable multiplayer on a per-game basis. Turning on additional controllers can disable single player controls in a handful of games
3. Right click a game, click `Edit Game Profile`
4. Click `Controller`
5. To the right of each Controller (`Controller 2` through `Controller 4`), select the respective `Deck #` profile (Deck 2 for player 2 and so on)
6. (Optional) You may need to re-arrange the controller order in Game Mode for your controllers to function as expected. See [How to Re-Arrange the Controller Order](../../../controls-and-hotkeys/steamos/external-controllers.md#how-to-re-arrange-the-controller-order) for more information

<img src="https://user-images.githubusercontent.com/108900299/226769760-abc659a8-4ddb-420b-9c33-b98043f27756.png" height="300">

---

### How to Use the Wii U Pro Controller Configuration

In some some games, the initial screen will prompt for a controller configuration: `Wii U Gamepad` or `Wii U Pro Controller`. Some games will automatically switch to the `Wii U Pro Controller` configuration if you choose it.

For example: <img src="https://user-images.githubusercontent.com/108900299/214977370-2e0fece0-4166-45ea-b373-5599b4d2b7ca.png" height="400">

If you prefer to use the `Wii U Pro Controller` layout, you need to change the controller profile in Cemu. Make sure to change controller profiles on a per-game basis so it is persistent on EmuDeck updates.

**Tutorial**

1. Right click the game, click `Edit game profile`
2. Click the `Controller` tab
3. Change the profile to `Deck-P1`
   <img src="https://user-images.githubusercontent.com/108900299/226769652-9696e8f7-a91e-46e7-a553-156037b7e39e.png" height="300">
4. When you launch a game, one of the following two things will happen:
   - Some games will prompt you to choose a controller layout, select the `Wii U Pro Controller`
   - Some games will automatically switch to the `Wii U Pro Controller` configuration

---

### How to Configure Cemu Native to Work With EmulationStation-DE

In order to use Cemu Native through EmulationStation-DE, you will have to enable it in the settings menu.

**Here's How**

1. Open EmulationStation-DE
2. Press `Start`
3. Press `Other Settings`
4. Press `Alternative Emulators`
5. On `Wiiu`, select `Cemu [Native]`

---

### How to Optimize Breath of the Wild

**IMPORTANT:** You need Version 208 of Breath of the Wild to use FPS++. Read [How to Manage DLC and Updates](#how-to-manage-dlc-and-updates) to learn how to install game updates for Cemu.

#### How to Configure Cemu

1. In Desktop Mode, open `Cemu AppImage`
2. Right click `Breath of the Wild`, click `Edit graphic packs`
   <img src="https://user-images.githubusercontent.com/108900299/236599933-8b568386-64ca-4bf3-8573-96c2374c46ce.png" height="300">
3. Click `Download latest community graphic packs`
4. Click the `⌄` to the left of `Mods`
5. Check the box to the left of `FPS++`
6. Change the mode to `Advanced Settings`
7. Change the `Framerate Limit` to `40FPS`
   <img src="https://user-images.githubusercontent.com/108900299/236599985-df1ac9fe-1c0f-48a0-8fcd-adb15688f71c.png" height="300">
8. Close out of Cemu

#### How to Configure Game Mode

1. In Game Mode, open Breath of the Wild
2. Click the `...` (the QAM) button
3. Click the battery icon
4. Click `Advanced View`
5. Enable `Use per-game profile`
6. Set the refresh rate to 40
   <img src="https://user-images.githubusercontent.com/108900299/236642316-5bafc264-6c82-479c-988a-b419515ee92b.png" height="300">

After doing the steps in the above two sections, Breath of the Wild will run at a stable 40 FPS with temporary occasional hiccups in new areas while it compiles shaders.

---

### How to Mod Breath of the Wild

This section will cover how to mod Breath of the Wild using UKMM, a mod manager.

1. In `/home/deck/Applications`, create a `ukmm` folder
   - These folders are recommendations, you may use a folder of your choice but you will need to adjust any paths in future steps to the folders you select
2. Download the latest `ukmm-x86_64-unknown-linux-gnu.tar.xz` file from [https://github.com/NiceneNerd/UKMM/releases](https://github.com/NiceneNerd/UKMM/releases) to `/home/deck/Applications/ukmm`
3. Right click `ukmm-x86_64-unknown-linux-gnu.tar.xz`, click `Extract archive here`
   - If it creates a subfolder, move the contents directly to `/home/deck/Applications/ukmm`
4. Download the attached `.sh` file and place it in `/home/deck/Applications/ukmm`
   - [ukmm-launcher.sh](../../configuration-files/ukmm-launcher.sh)
   - For the contents of the script, see [https://raw.githubusercontent.com/EmuDeck/emudeck.github.io/main/docs/configuration-files/ukmm-launcher.sh](https://raw.githubusercontent.com/EmuDeck/emudeck.github.io/main/docs/configuration-files/ukmm-launcher.sh)
   - If you used a different folder than what was recommended in Step 1, make sure to open `ukmm-launcher.sh` in Kate or a text editor of your choice and update the paths to where you placed UKMM
5. Right click `ukmm-launcher.sh`, click `Properties`, click `Permissions`, check `Is Executable`
   - Use this file whenever you want to launch UKMM
   - You may add UKMM to Steam by right clicking it and clicking `Add to Steam`
6. Double click `ukmm-launcher.sh` to open it
7. Follow UKMM's documentation, [https://nicenenerd.github.io/UKMM/using-mods.html](https://nicenenerd.github.io/UKMM/using-mods.html) to learn how to mod Breath of the Wild
   - When deploying mods, the graphic pack folder will be located here: `/home/deck/.local/share/Cemu/graphicPacks`

---

### How to Roll Back Cemu to an Older Version

#### Preface

Your ROMs launch using a script created by EmuDeck, `cemu.sh` in `Emulation/tools/launchers`.

The script launches the corresponding emulator in `/home/deck/Applications` and **specifically looks** for two traits:

- The most recently downloaded version of the emulator in `/home/deck/Applications`, based on the file/release date.
- The emulator name at the beginning of the file. Anything after the emulator name is ignored.
  - For example, if the latest version of the emulator is `1351` and you would like to downgrade to `1349`. When you download version `1349`, you could rename it to `EMULATORNAME-1349.AppImage`, and EmuDeck's script will ignore the `-1349` in the file name, allowing you to record which versions of the emulator you are using through the file name.

#### How to Roll Back Cemu

1. Download the version of the emulator you would like to use from Cemu's GitHub: [https://github.com/cemu-project/Cemu/releases](https://github.com/cemu-project/Cemu/releases)
2. Move the downloaded emulator from Step 1 to `/home/deck/Applications`
3. (Optional) Rename or delete the original emulator file
4. Right click the newly downloaded emulator, click `Properties`, click `Permissions`, check `Is executable`
5. Your games will now launch using the version of the emulator you downloaded

---

### How to Configure Language Settings

#### UI

1. In Desktop Mode, open Cemu
2. Click `Options` at the top
3. Under `Interface`, click the `Language` drop-down menu and select your preferred language
4. Restart Cemu

#### In-Game

1. In Desktop Mode, open Cemu
2. Click `Options` at the to
3. Click `Console language` and select your preferred language

---

### How to Configure Online Multiplayer Via Pretendo

You need a **physical Wii U** to play online multiplayer via Pretendo. You **cannot** play online multiplayer without a physical Wii U.

For instructions on how to dump the online files from a Wii U, see [https://cemu.cfw.guide/using-dumpling.html#copying-online-files-to-cemu](https://cemu.cfw.guide/using-dumpling.html#copying-online-files-to-cemu).

For more information on Pretendo, see [https://pretendo.network/](https://pretendo.network/).

For Pretendo's installation instructions, see [https://pretendo.network/docs/install/cemu](https://pretendo.network/docs/install/cemu).

1. From your Wii U, you will need to dump two files: `otp.bin` and `seeprom.bin`
2. On the Steam Deck, place these two files directly in the `$HOME/.local/share/Cemu` folder
   - Folders with a `.` (`.var`, `.local`, `.config`, etc.) at the beginning are hidden by default. In Dolphin (file manager), click the hamburger menu in the top right, click `Show Hidden Files` to see these folders
3. In Desktop Mode, open Cemu, click `Options`, `General Settings`, click `Account`, select your `PNID` in the `Active Account` drop-down menu and select `Pretendo` under `Network Service`
4. Pretendo is now configured for Cemu

---
