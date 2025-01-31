# <img src="/assets/emulators/melonds.png" alt="EmuDeck guide" width="80" style="vertical-align: middle"> melonDS Tips and Tricks

[TOC]

---

### Open Source BIOS



The open source BIOS is **enabled by default** for melonDS. This means that BIOS for Nintendo DS games is **optional**. However, some games may not perform as expected with the open source BIOS or you may need additional features provided by console dumped BIOS. You may also prefer to use DSI BIOS which allow you to play DSIWare games.

In order to use console dumped BIOS, you may place the files required into the `Emulation/bios` folder. You will also need to enable `Use external BIOS/firmware files` in the melonDS GUI.

![melonDS Open Source BIOS](../../assets/melonds-open-source-bios.png)

---

### How to Configure Multiplayer



This section is strictly referring to local multiplayer. melonDS multiplayer on the Steam Deck can only be done in Desktop Mode.

1. In Desktop Mode, open melonDS
2. Click `System`, click `Multiplayer`, `Launch new instance`
3. On each window of melonDS, click `Config`, `Input and hotkeys`
4. In the drop-down menu to the right of `Joystick`, select your controller
   - Steam Deck/Player 1: `Microsoft X-Box 360 pad 0`
   - Player 2: `Microsoft X-Box 360 pad 1`
   - Player 3: `Microsoft X-Box 360 pad 2`
   - Player 4: `Microsoft X-Box 360 pad 3`
5. Open the game in each melonDS window and you will be able to play multiplayer

You can determine which melonDS window corresponds to what player by looking at the menu bar at the top. Each new melonDS window will have a corresponding `(#)`.

---

### How to Configure Settings



#### Game Mode

If you are playing in Game Mode, make sure you have the correct "Steam Input" profile applied. For more information, see the [Hotkeys](#melonds-hotkeys) section.

While in game, press `Select` + `R3` to exit full screen. While melonDS is windowed, you will have access to the settings at the top of the screen. Adjust these options to your liking. After you have made your changes, press `Select` + `R3` again to switch melonDS back to full screen.

After you have made your changes and you are ready to exit your game, **do not** use the `STEAM` butto to exit out of the game. If you use the `STEAM` button, any changes you have made will be reverted.

Press `Select` + `R3` again to exit full screen. In the top right, click `File`, click `Quit`. You will only need to do this when you are changing settings. Otherwise, you may simply use the `STEAM` button as usual.

#### Desktop Mode

In Desktop Mode, open melonDS. Adjust any options to your liking. In the top right, click `File`, click `Quit`.

**Do not** click the `X` button in the top right to exit out of melonDS. If you use the `X` button, any changes will be reverted.

---

### How to Use Cheats



**Note:** melonDS does not currently support importing cheats from a database file.

#### How to Enable Cheats in melonDS

1. Open melonDS
2. Click `System` at the top
3. Check `Enable cheats`
   <img src="https://user-images.githubusercontent.com/108900299/220514789-7511568d-4806-4528-8521-ea1d6e35b989.png" height="300">

#### How to Download the Cheats Database

1. Open [https://db.universal-team.net/ds/ndsi-cheat-databases](https://db.universal-team.net/ds/ndsi-cheat-databases), right click `cheats.xml`, and click `Save As`
2. Place it in `Emulation/storage/melonds/cheats`
   - This folder placement is optional, you may place it wherever you want
3. To view, right click `cheats.xml`, open with a text editor of your choice

#### How to Use the Cheats Database

**Note:** It's recommended you do this in Desktop mode so you can easily copy from the cheats database into MelonDS. After adding cheats, you can use MelonDS in Game Mode.

1. Open the `cheats.xml` you downloaded from the `How to Download the Cheats Database` section
2. `CTRL` + `F` the game you are adding cheats to
3. Copy the blocks of alphanumerical strings between the two `<codes> <codes>` for your respective cheat
   - Example: <img src="https://user-images.githubusercontent.com/108900299/220517493-9305654f-660e-4845-8210-ea1da61ce2b2.png" height="300">
4. Open MelonDS
5. Open a ROM
6. Click `System` at the top
7. Click `Setup cheat codes`
8. Create a `New Category`, you may name it whatever you would like
9. Click `New AR Code`
10. Match the name of the AR Code to the cheat you located in Step 3

- The name is flexible, you may name it whatever you would like

11. Paste the code you copied from Step 3, it will appear as red text
12. Format the cheat so there are two blocks of code per line
    - Original: <img src="https://user-images.githubusercontent.com/108900299/220517044-dc4c547b-7a13-4a42-aa34-c3f36786c320.png" height ="300">
    - Corrected: <img src="https://user-images.githubusercontent.com/108900299/220516960-47147c37-d914-4ced-9893-f5b9c9e47781.png" height="300">
13. Some cheats are automatically activated, others will require a button combo. Look at the `cheats.xml` file to see if a button combo is required to activate your cheat

---

### How to Set Up DSIWare



The Nintendo DSI requires DSI specific BIOS. Place **all** of the files from the list below **directly** in `Emulation/bios`.

- `dsi_bios9.bin`
- `dsi_bios7.bin`
- `dsi_firmware.bin`
- `dsi_nand.bin`

**Note:**

- The BIOS must be named exactly as above. BIOS with any deviations from the above **will not** work. Make sure you have the proper casing, characters, and spelling.
- BIOS must be placed in `Emulation/bios`. If you create a sub-folder, the BIOS will not be picked up and Nintendo DSI games **will not** work.

---

**Preface:** Generally, DSIWare games are named `00000000` with no file extension. This section assumes you have these types of DSIWare ROMs.

1. Place your DSI BIOS in `Emulation/bios`
2. Place your DSIWare ROMs in `Emulation/roms/nds`
3. Right click the DSIWare ROM in `Emulation/roms/nds`, click `Rename`, rename it from `00000000` to `GAMENAME.app`
   - Replace `GAMENAME` with the name of the DSIWare game
   - For example:
     - Original file name: `00000000`
     - Updated file name: `X-Scape.app`
4. In Desktop Mode, open melonDS
5. At the top, select `Config`, `Emu Settings`
6. On the `General` tab, change the `Console type` to `DSi (experimental)`
   - ![How to Set Up DSIWare 1](../../assets/how-to-set-up-dsiware-1.png)
7. On the `DS-mode` tab, check `Use external BIOS/firmware files`, close out of this menu
   - ![How to Set Up DSIWare 2](../../assets/how-to-set-up-dsiware-2.png)
8. At the top, select `System`, `Manage DSi titles`
9. On the `DSi Title Manager` screen, select `Import title`
10. Select your `GAMENAME.app` as the `Executable`
11. Under `Metadata`, select `Download from NUS`, close out of this menu
12. Select `File`, `Boot Firmware`
13. Select your newly-installed DSiWare game and start playing

---

#### Steam ROM Manager and ES-DE

Both EmuDeck's Steam ROM Manager parser for melonDS (Standalone) and ES-DE support the `.app` file extension. As long as your DSIWare ROMs are in `Emulation/roms/nds`, you may use either option to play your DSIWare ROMs in Game Mode.

Do note that your ROM may not have art on SteamGridDB or metadata on ES-DE's scraping websites. Follow the links below if you would like to add art or metadata to one of these websites.

- Steam ROM Manager
  - [SteamGridDB](https://www.steamgriddb.com/)
    - You may request a game page here: [https://www.steamgriddb.com/request-game](https://www.steamgriddb.com/request-game)
      - You will need to login to view this page
- ES-DE
  - [TheGamesDB](https://thegamesdb.net/)
  - [ScreenScraper](https://www.screenscraper.fr/)

---

### How to Play Nintendo DS Games in Book Mode



A handful of Nintendo DS games require portrait orientation. For these games, you will need to rotate the Steam Deck screen in order to play them. Fortunately, it's a simple process.

**Here's How**

1. In Game Mode, select the `EmuDeck - Controller Hotkeys` profile if you are playing a game directly from Game Mode or the `EmuDeck - Frontend Controller Hotkeys` profile if you are playing through ES-DE or Pegasus
   - [How to Select a Steam Input Profile](../../controls-and-hotkeys/steamos/hotkeys.md#how-to-select-a-steam-input-profile)
2. Open the game, use the Steam Input profile and select the `Fullscreen` hotkey
3. At the top, press `Config`, `Screen Rotation`, `270`
   <img src="https://user-images.githubusercontent.com/108900299/224400268-181fd70c-3ef1-470d-85ef-9a8897211958.png" height="300">
   <img src="https://user-images.githubusercontent.com/108900299/224400552-b53ddd81-c448-473e-9951-5003cb8b6b14.png" height="300">

---

Original: <img src="https://user-images.githubusercontent.com/108900299/224400685-7f8b98be-b75b-4758-9d84-07ae3e5f8179.png" height="300">

Rotated: <img src="https://user-images.githubusercontent.com/108900299/224400804-2155e870-d6fd-4e3b-8b6b-2ecf47812db8.png" height="300">

---

### How to Customize the Screen Layout

By default, EmuDeck configures melonDS' screens to use a hybrid layout, meaning there is a large top screen on the left side of the screen and a mini top and bottom screen of the Nintendo DS on the right. If you would rather a different layout, it is fairly easy to customize.

**Here's How**

1. In Game Mode, select the `EmuDeck - Controller Hotkeys` profile if you are playing a game directly from Game Mode or the `EmuDeck - Frontend Controller Hotkeys` profile if you are playing through ES-DE or Pegasus
   - [How to Select a Steam Input Profile](../../controls-and-hotkeys/steamos/hotkeys.md#how-to-select-a-steam-input-profile)
2. Open the game, use the Steam Input profile, and click `Select` + `R3`
3. At the top, press `Config`, and use `Screen size`, `Screen rotation`, `Screen layout`, `Screen sizing`, and `Aspect Ratio` to customize your layout
   <img src="https://github.com/dragoonDorise/EmuDeck/assets/108900299/93413e6c-a704-48ea-aaca-565f54a85bb6" height="300">
4. When you are finished playing your game, click `Select` + `R3` again. In the top right, click `File`, click `Quit`. If you use the `STEAM` button to exit out of the game, any changes you have made **will not** be saved

The `Screen layout` is where you can find the `Hybrid layout` option. Here, you can swap to `Natural`, `Vertical`, `Horizontal`, and `Hybrid`.

**How to Reset to EmuDeck Defaults**

If you configured the settings and you decide you would like to reset to EmuDeck's defaults, you can do so by following the below:

1. Open the EmuDeck application in Desktop Mode
2. Click the `Manage Emulators` page
3. Click `melonDS` and click `Reset Configurations`

**How to Back Up your Screen Layout Configuration**

1.  In Desktop Mode, open `/home/deck/.var/app/net.kuribo64.melonDS/config/melonDS`
    - `~/.var` is an invisible folder by default. In Dolphin (file manager), click the hamburger menu in the top right, click `Show hidden files` to see these folders
2.  Open `melonDS.ini` in Kate or a text editor of your choice
3.  Copy the following section to another file:

            WindowWidth=1280
            WindowHeight=771
            WindowMax=0
            ScreenRotation=0
            ScreenGap=0
            ScreenLayout=3
            ScreenSwap=0
            ScreenSizing=3
            IntegerScaling=0
            ScreenAspectTop=4
            ScreenAspectBot=4

4.  Back up this file to a secure location. If/when your melonDS configs are reset on an EmuDeck update, you may paste this section into the `melonDS.ini` to restore your custom layout

---

### How to Roll Back melonDS to an Older Version



If you do not have access to a mouse and keyboard for the below section, use `L2` to right click and `R2` to left click. Alternatively, remote into your Steam Deck using one of the methods found in the FAQ, [How do I remotely control my Steam Deck?](../../frequently-asked-questions/steamos/index.md#how-do-i-remotely-control-my-steam-deck).

1. In Desktop Mode, open `Konsole`
2. To see a list of prior versions of the emulator, type:
   - `flatpak remote-info --log flathub net.kuribo64.melonDS`
3. If Konsole prompts you to select `system` or `user`, enter `2` to select `user`
4. Konsole will list a list of previous versions for the flatpak. The important line for each version is the `Commit: ` line. The `Commit: ` line will have a long accompanying alphanumeric string (the “commit” code). Copy the string for the version you want to downgrade to.
   - Using Citra as an example:
     - ![How to Roll Back Flatpaks: 1](../../assets/how-to-roll-back-flatpaks-1.png)
5. To downgrade to the version you want:
   - `flatpak update --commit=put_commit_code_here net.kuribo64.melonDS`
   - Replace `put_commit_code_here` with the actual code you located in Step 2.
     - Using Citra as an example:
       - ![How to Roll Back Flatpaks: 2](../../assets/how-to-roll-back-flatpaks-2.png)

If the above steps did not work and you are getting an error message along the lines of `Flatpak not installed`, your Flatpak is likely installed at the system level instead. Select one of the below solutions:

Solution 1: Open the EmuDeck application, click the `Manage Emulators` page, select the emulator in question, and click `Reinstall / Update`.

Solution 2: Add `sudo` in front of the commands written in Step 2 and Step 5. In Step 2, write `sudo flatpak remote-info --log flathub net.kuribo64.melonDS` and in Step 5, write `sudo flatpak update --commit=put_commit_code_here net.kuribo64.melonDS`.

---

### How to Configure Language Settings



#### In-Game

Some games may not have language options. For a full list of which games have language options, download the DS Database from GamesTDB, [https://www.gametdb.com/DS/Downloads](https://www.gametdb.com/DS/Downloads) and open it in a text editor of your choice.

Before proceeding with the below section, you will need to place Nintendo DS BIOS in the `Emulation/bios` folder.

1. In Desktop Mode, open melonDS
2. At the top, click `Config`
3. Click `Emu settings`
4. Click `DS-Mode`, check `Use external BIOS/firmware files`
5. Close out of the `Emu settings` window
6. Click `File`, click `Boot firmware`
7. Click the DS icon at the bottom of the screen
8. Click the gear icon
9. Click the globe icon
10. Select your preferred language

---
