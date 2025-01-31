# <img src="/assets/emulators/rmg.png" alt="EmuDeck guide" width="80" style="vertical-align: middle"> RMG Tips and Tricks

[TOC]

---

### How to Configure Multiplayer



EmuDeck configures multiplayer out of the box. You do not need to configure the controls. To set up multiplayer, you simply need to enable the additional ports.

**Tutorial**

1. Open Rosalie's Mupen GUI
2. Open the `Input` settings
3. For each controller you are using for Player 2, 3, and 4, click the respective tab
   - You do not need to adjust any settings for Player 1
4. Under `Input Device`
   - Player 2: `Steam Virtual Gamepad 1`
   - Player 3: `Steam Virtual Gamepad 2`
   - Player 4: `Steam Virtual Gamepad 3`
5. Under `Profile`
   - Player 2: `steamdeck2`
   - Player 3: `steamdeck3`
   - Player 4: `steamdeck4`
6. After you are finished enabling any additional players, click `OK` and you may open your game either directly as a shortcut in Steam or through EmulationStation-DE
7. (Optional) You may need to re-arrange the controller order in Game Mode for your controllers to function as expected. See [How to Re-Arrange the Controller Order](../../controls-and-hotkeys/steamos/external-controllers.md#how-to-re-arrange-the-controller-order) to learn how

---

### How to Install Custom Textures



#### Preface

HTS & HTC are cache formats. PNG is the 'source' of the texture packs before it's converted to a cache file.

Before installing a texture pack, you will need to determine if it is HTC, HTS, or PNG. This can usually be confirmed by checking the file extension or reading the attached documentation. Follow the respective section below for installing texture packs.

#### Keep in Mind

- This section specifically requires the GLideN64 plugin. GLideN64 is the default graphics plugin if you are using EmuDeck settings
- Texture packs are placed in the various subfolders within `Emulation/storage/RMG`
  - This folder contains the following sub-folders:
    - `cache`
      - `cache` is for HTC and HTS texture packs
    - `HiResTextures`
      - `HiResTextures` is for PNG texture packs

#### Texture Pack Sources

_This list is not exhaustive_

- [https://evilgames.eu/texture-packs.htm](https://evilgames.eu/texture-packs.htm)
- [https://www.n64textures.com/downloads/?lang=en](https://www.n64textures.com/downloads/?lang=en)
- [https://emulationking.com/category/n64-texturepacks/](https://emulationking.com/category/n64-texturepacks/)

---

#### How to Install Custom Textures

##### HTC

1. Open the `Emulation/storage/RMG/cache` folder
2. Place your texture pack file directly into this folder
3. Open RMG
4. Click `Settings` at the top, select `Graphics`
5. Click the `Texture enhancement` tab
6. Make sure `Use file storage instead of memory cache` is unchecked
   <img src="https://user-images.githubusercontent.com/108900299/220504844-73ad1aae-9525-4e07-aa46-a47bcf953a8e.png" height="300">
   - This setting is unchecked by default

##### HTS

1. Open the `Emulation/storage/RMG/cache` folder
2. Place your texture pack file directly into this folder
3. Open RMG
4. Click `Settings` at the top, select `Graphics`
5. Click the `Texture enhancement` tab
6. Check `Use file storage instead of memory cache`
   <img src="https://user-images.githubusercontent.com/108900299/220504446-d29fc261-9194-43ee-ba19-2c15562ac716.png" height="300">
   - **Note:** To save this setting on a per game basis, you can open the graphics settings while in-game and it will save to the per-game profile

##### PNG

This section goes over enabling `file storage instead of memory cache` in RMG's settings. This is optional, but recommended.

1. Open the `Emulation/storage/RMG/HiResTextures` folder
2. Place your texture pack folder directly into this folder
3. Open RMG
4. Click `Settings` at the top, select `Graphics`
5. Click the `Texture enhancement` tab
6. Check `Use file storage instead of memory cache`
   <img src="https://user-images.githubusercontent.com/108900299/220504446-d29fc261-9194-43ee-ba19-2c15562ac716.png" height="300">
   - **Note:** To save this setting on a per game basis, you can open the graphics settings while in-game and it will save to the per-game profile

---

### How to Configure VRU



The VRU (Voice Recognition Unit) was a peripheral for the Nintendo 64 that allowed you to use a microphone in "Hey You, Pikachu!" and "Densha de Go! 64".

Since the Steam Deck comes with an internal built in microphone, you can use the Steam Deck's microphone to utilize VRU in Rosalie's Mupen GUI.

**Note:** Make sure Rosalie's Mupen GUI is up to date. VRU support was added in v0.4.2, on July 7th, 2023.

#### How to Set up VRU

1. Open RMG
2. Open the `Input` settings under the `Settings` tab at the top
3. Click on `Player 4`
4. Change the `Input Device` to `Voice Recognition Unit`
   - ![RMG VRU](../../assets/rmg-vru.png)
5. Click `OK` in the bottom right
6. VRU is now enabled

---

### How to Configure N64DD



The Nintendo 64DD was a floppy disk drive peripheral for the Nintendo 64.

See [https://en.wikipedia.org/wiki/64DD#Games](https://en.wikipedia.org/wiki/64DD#Games) for a full list of Nintendo 64DD games.

Nintendo 64DD requires region specific BIOS. Place the respective BIOS from the list below directly in `Emulation/bios` matching the region of your Nintendo 64DD game.

- `64DD_IPL_US.n64`
- `64DD_IPL_JP.n64`
- `64DD_IPL_DEV.n64`

**Note:**

- The BIOS must be named exactly as above. BIOS with any deviations from the above **will not** work. Make sure you have the proper casing, characters, and spelling.
- BIOS must be placed in `Emulation/bios`. If you create a sub-folder, the BIOS will not be picked up and Nintendo 64DD games **will not** work.

---

For the following games, place the Nintendo 64DD ROM in `Emulation/roms/n64` or `Emulation/roms/n64dd`, **no** additional set-up is required. These games are plug and play.

To play your games directly through Rosalie's Mupen GUI, your ROMs must be placed in `Emulation/roms/n64`. To use Steam ROM Manager or EmulationStation-DE, your ROMs may be either in `Emulation/roms/n64` or `Emulation/roms/n64dd`.

Either parse your Nintendo 64DD games through the `Nintendo 64 - RMG` parser in Steam ROM Manager or play them directly through EmulationStation-DE.

- Mario Artist: Paint Studio
- Doshin the Giant
- Mario Artist: Talent Studio
- SimCity 64
- Japan Pro Golf Tour 64
- Doshin the Giant: Tinkling Toddler Liberation Front! Assemble!
- Mario Artist: Communication Kit
- Mario Artist: Polygon Studio

**Note:** Mario Artist will boot but the mouse peripheral is not supported at this time.

---

**For the F-Zero X Expansion Kit, follow the below steps**

1. Place your base Nintendo 64 `F-Zero X` ROM in `Emulation/roms/n64` and the `F-Zero X Expansion Kit` N64DD ROM in `Emulation/roms/n64dd`
   - The regions for the base ROM and the expansion kit need to match. If you are using the Japanese `F-Zero X Expansion Kit` ROM, you need a Japanese `F-Zero X` ROM
2. Right click `F-Zero X`, click `Edit Game Settings`
3. Click the `Core` tab under the `Game` tab
4. Check `Override Core Settings`
5. Change the `CPU Emulator` to `Cached Interpreter`, close out of the settings menu
6. Right click the base `F-Zero X` ROM, click `Play Game With Disk` and select the `F-Zero X Expansion Kit` N64DD ROM in `Emulation/roms/n64dd`

---

**Optional: How to Add F-Zero X Expansion Kit directly to Steam**

1. Place your base Nintendo 64 `F-Zero X` ROM in `Emulation/roms/n64` and the `F-Zero X Expansion Kit` N64DD ROM in `Emulation/roms/n64dd`
2. Parse your base `F-Zero X` ROM through the `Nintendo 64 - RMG` parser in Steam ROM Manager
3. In Desktop Mode, open Steam, select the `F-Zero X` ROM, click the `Gear` icon, click `Properties`
   - ![F-Zero X Expansion Kit 1](../../assets/f-zero-x-expansion-kit-1.png)
4. Scroll to the end of the `Launch Options` box and add `--disk "/path/to/F-Zero X Expansion Kit"` (write the path with the quotes)
   - ![F-Zero X Expansion Kit 2](../../assets/f-zero-x-expansion-kit-2.png)

---

### How to Use Cheats



#### Mid-Game

1. While in game, use the left Trackpad and select the `Cheats` icon
   - Steam Input profiles for Nintendo 64 ROMs and EmulationStation-DE are enabled by default. However, if you do not see the Trackpad menu, see [How to Select a Steam Input Profile](../../controls-and-hotkeys/steamos/hotkeys.md#how-to-select-a-steam-input-profile)
2. Select which cheats you would like to use

#### Emulator

1. Open Rosalie's Mupen GUI
2. Right click a game
3. Click `Edit cheats`
   - If you would like to add new cheats, it is recommended you do so in Desktop Mode

---

### How to Roll Back RMG to an Older Version



If you do not have access to a mouse and keyboard for the below section, use `L2` to right click and `R2` to left click. Alternatively, remote into your Steam Deck using one of the methods found in the FAQ, [How do I remotely control my Steam Deck?](../../frequently-asked-questions/steamos/index.md#how-do-i-remotely-control-my-steam-deck).

1. In Desktop Mode, open `Konsole`
2. To see a list of prior versions of the emulator, type:
   - `flatpak remote-info --log flathub com.github.Rosalie241.RMG`
3. If Konsole prompts you to select `system` or `user`, enter `2` to select `user`
4. Konsole will list a list of previous versions for the flatpak. The important line for each version is the `Commit: ` line. The `Commit: ` line will have a long accompanying alphanumeric string (the “commit” code). Copy the string for the version you want to downgrade to.
   - Using Citra as an example:
     - ![How to Roll Back Flatpaks: 1](../../assets/how-to-roll-back-flatpaks-1.png)
5. To downgrade to the version you want:
   - `flatpak update --commit=put_commit_code_here com.github.Rosalie241.RMG`
   - Replace `put_commit_code_here` with the actual code you located in Step 2.
     - Using Citra as an example:
       - ![How to Roll Back Flatpaks: 2](../../assets/how-to-roll-back-flatpaks-2.png)

If the above steps did not work and you are getting an error message along the lines of `Flatpak not installed`, your Flatpak is likely installed at the system level instead. Select one of the below solutions:

Solution 1: Open the EmuDeck application, click the `Manage Emulators` page, select the emulator in question, and click `Reinstall / Update`.

Solution 2: Add `sudo` in front of the commands written in Step 2 and Step 5. In Step 2, write `sudo flatpak remote-info --log flathub com.github.Rosalie241.RMG` and in Step 5, write `sudo flatpak update --commit=put_commit_code_here com.github.Rosalie241.RMG`.

---

### How to Configure Language Settings



#### In-Game

Some games may not have language options. For a full list of which games have language options, click one of the below links.

- NTSC-U: [http://micro-64.com/database/languagesntsc.shtml](http://micro-64.com/database/languagesntsc.shtml)
- PAL: [http://micro-64.com/database/languagespal.shtml](http://micro-64.com/database/languagespal.shtml)

1. Launch a game that supports your preferred language
2. Depending on the game:
   - Select your preferred language on the initial launch of the game
   - In the main menu of the game, open the Options menu and select your preferred language

---
