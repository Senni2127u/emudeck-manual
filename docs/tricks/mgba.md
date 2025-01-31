# <img src="/assets/emulators/mgba.png" alt="EmuDeck guide" width="80" style="vertical-align: middle"> mGBA Tips and Tricks

[TOC]

---

### How to Configure Multiplayer



This section is strictly referring to local multiplayer. mGBA multiplayer on the Steam Deck can only be done in Desktop Mode.

1. In Desktop Mode, open mGBA
2. Click `File`, click `New multiplayer window`
3. On each window of mGBA, click `Tools`, `Settings`
4. Select `Controllers` on the left and select your controller in the drop-down menu
   - Steam Deck/Player 1: `Microsoft X-Box 360 pad 0`
   - Player 2: `Microsoft X-Box 360 pad 1`
   - Player 3: `Microsoft X-Box 360 pad 2`
   - Player 4: `Microsoft X-Box 360 pad 3`
5. Open the game in each mGBA window and you will be able to play multiplayer

If you are intending on trading with yourself (in a Pokemon game as an example), you will need to create a second copy of your save file and rename the file extension to `.sa2`.

---

### How to Use the Gyro Sensor



**IMPORTANT:** As of September 2023, there is a bug with rumble while using gyro. Keeping rumble enabled will severly impact your framerate. Open the mGBA emulator and disable the rumble feature if you intend on using gyro.

**Supported Games**

- WarioWare: Twisted!

**Note:** Yoshi Topsy-Turvy and Kirby Tilt 'n' Tumble use the tilt sensor instead. Read: [How to Use the Tilt Sensor](#how-to-use-the-tilt-sensor) for instructions.

- [How to Configure the Gyro Sensor for the Steam Deck](#how-to-configure-the-gyro-sensor-for-the-steam-deck)
- [How to Configure the Gyro Sensor for Non Steam-Deck Controllers](#how-to-configure-the-gyro-sensor-for-non-steam-deck-controller)

#### How to Configure the Gyro Sensor for the Steam Deck

##### How to Configure mGBA

1.  Open `/home/deck/.config/mgba`
    - `~/.config` is an invisible folder by default. In Dolphin (file manager), click the hamburger menu in the top right, click `View hidden files`
2.  Right click `config.ini`, click `Open with Kate` or a text editor of your choice
3.  Under `gba.input-profile.03000000de280000ff11000001000000`, use the following template:

            tiltAxisY=4
            gyroAxisX=3
            gyroAxisZ=3
            gyroSensitivity=2.2e+09
            tiltAxisX=2
            gyroAxisY=1

4.  Save the file and exit out
5.  Open mGBA
6.  Click `Tools` at the top
7.  Click `Game Pak sensors...`
8.  Set the sensitivity in the bottom right to `34`

##### How to Configure Steam Input

1.  In Game Mode, select the `WarioWare: Twisted!` ROM or the mGBA emulator
2.  Click the `Controller` icon
3.  Change the layout to `EmuDeck - mGBA`
4.  Click `Edit Layout`
5.  Select `Gyro` on the left
6.  Gyro Behavior: `As Joystick`
7.  Click the `Gear` icon
8.  Use the following template:

            Gyro Output Scale: 60
            Gyro Enable Button: Select a behavior of your choice
            Minimum Joystick X Output Value: 1
            Minimum Joystick Y Output Value: 1

9.  Back out, and select `Joysticks` on the left
10. Click the `Gear` icon to the right of `Right Joystick Behavior`
11. Set `Deadzone Type` to `Default`

---

#### How to Configure the Gyro Sensor for Non Steam-Deck Controllers

1. In Desktop Mode, connect your non-Steam Deck controller
2. Open mGBA in Desktop Mode
3. Click `Tools`
4. Click `Settings`
5. Click `Controllers` on the left
6. Select your controller in the drop-down menu
7. Click `OK`
8. Click `Tools`, `Game Pak Sensors`, and test your controller

#### Post-Configuration

To restore the default Steam Deck controls:

1. Open mGBA in Desktop Mode
2. Click `Tools`
3. Click `Settings`
4. Click `Controllers` on the left
5. Select `Microsoft X-Box 360 pad 0` in the drop-down menu

---

### How to Use the Tilt Sensor



**Supported Games**

- Kirby Tilt 'n' Tumble
- Koro Koro Puzzle Happy Panechu!
- Yoshi Topsy-Turvy

**Note:** For WarioWare: Twisted!, use the gyro sensor instead. Read: [How to Use the Gyro Sensor](#how-to-use-the-gyro-sensor) for instructions.

- [How to Configure the Tilt Sensor for the Steam Deck](#how-to-configure-the-tilt-sensor-for-the-steam-deck)
- [How to Configure the Tilt Sensor for Non Steam-Deck Controllers](#how-to-configure-the-tilt-sensor-for-non-steam-deck-controller)

---

#### How to Configure the Tilt Sensor for the Steam Deck

mGBA does not support using the Steam Deck's accelerometer for the tilt sensor at this time. Instead, you may either use a patch to remove the requirement for the tilt sensor or use an external controller.

---

#### Tilt Sensor Patches

To learn how to use these patches, see [How to Use ROM Hacks](../../community-creations/steamos/tools-and-guides.md#how-to-use-rom-hacks).

- Kirby Tilt 'n' Tumble
  - [https://gbatemp.net/threads/kirby-tilt-n-tumble-gbc-tilt-fix-accelerometer-removal-patch.605800/](https://gbatemp.net/threads/kirby-tilt-n-tumble-gbc-tilt-fix-accelerometer-removal-patch.605800/)
- Koro Koro Puzzle Happy Panechu!
  - [https://gbatemp.net/threads/yoshitt-warioware-korokoro-no-tilt-patches.584171/](https://gbatemp.net/threads/yoshitt-warioware-korokoro-no-tilt-patches.584171/)
- Yoshi Topsy-Turvy
  - [https://gbatemp.net/threads/yoshitt-warioware-korokoro-no-tilt-patches.584171/](https://gbatemp.net/threads/yoshitt-warioware-korokoro-no-tilt-patches.584171/)

---

#### How to Configure the Tilt Sensor for Non Steam-Deck Controllers

1. In Desktop Mode, connect your non-Steam Deck controller
2. Open mGBA in Desktop Mode
3. Click `Tools`
4. Click `Settings`
5. Click `Controllers` on the left
6. Select your controller in the drop-down menu
7. Click `OK`
8. Click `Tools`, `Game Pak Sensors`, and test your controller

#### Post-Configuration

To restore the default Steam Deck controls:

1. Open mGBA in Desktop Mode
2. Click `Tools`
3. Click `Settings`
4. Click `Controllers` on the left
5. Select `Microsoft X-Box 360 pad 0` in the drop-down menu

---

### How to Use Cheats



**Cheat Resources**

_This list is not comprehensive_

- [https://gamehacking.org](https://gamehacking.org)
  - [Game Boy](https://gamehacking.org/system/gb)
  - [Game Boy Color](https://gamehacking.org/system/gbc)
  - [Game Boy Advance](https://gamehacking.org/system/gba)

#### Desktop Mode

1. In Desktop Mode, open mGBA
2. Load a game
3. Click `Tools` at the top
4. Click `Cheats`
5. Click `Add New Code`
6. Add your cheat

#### Game Mode

1. While in game, use the left Trackpad and select the `Cheats` icon
   - Steam Input profiles for mGBA ROMs and ES-DE are enabled by default. However, if you do not see the Trackpad menu, see [How to Select a Steam Input Profile](../../controls-and-hotkeys/steamos/hotkeys.md#how-to-select-a-steam-input-profile)
2. Select which cheats you would like to use

---

### How to Roll Back mGBA to an Older Version



#### Preface

Your ROMs launch using a script created by EmuDeck, `mgba.sh` in `Emulation/tools/launchers`.

The script launches the corresponding emulator in `/home/deck/Applications` and **specifically looks** for two traits:

- The most recently downloaded version of the emulator in `/home/deck/Applications`, based on the file/release date.
- The emulator name at the beginning of the file. Anything after the emulator name is ignored.
  - For example, if the latest version of the emulator is `1351` and you would like to downgrade to `1349`. When you download version `1349`, you could rename it to `EMULATORNAME-1349.AppImage`, and EmuDeck's script will ignore the `-1349` in the file name, allowing you to record which versions of the emulator you are using through the file name.

#### How to Roll Back mGBA

1. Download the version of the emulator you would like to use from mGBA's GitHub: [https://github.com/mgba-emu/mgba/releases](https://github.com/mgba-emu/mgba/releases)
2. Move the downloaded emulator from Step 1 to `/home/deck/Applications`
3. (Optional) Rename or delete the original emulator file
4. Right click the newly downloaded emulator, click `Properties`, click `Permissions`, check `Is executable`
5. Your games will now launch using the version of the emulator you downloaded

---

### How to Configure Language Settings



#### UI

1. In Desktop Mode, open mGBA
2. At the top, click `Tools`, click `Settings`
3. Click the `Interface` tab
4. To the right of `Language`, select your preferred language in the drop-down menu

#### In-Game

Languages are cartridge-specific. For example, if you want to play Golden Sun in French, you will need to dump a Golden Sun cartridge from France.

---

### How to Create Multiple Save Files for a Game



If you would like to create multiple saves for a game in games where multiple save options are not available (the Pokemon games for example), you can do so by creating unique save files for the game.

1. While in game, press `Start` + `L3`
2. At the top, click `File`
3. Click `Save Games`
4. Select your preferred save slot, `Use Player # save game`

---
