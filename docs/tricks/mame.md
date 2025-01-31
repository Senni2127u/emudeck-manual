# <img src="/assets/emulators/mame.png" alt="EmuDeck guide" width="80" style="vertical-align: middle"> MAME Tips and Tricks

[TOC]

---

### Maintaining ROM Versions



Ideally use ROMs that are the same version as MAME's version. MAME often releases improved versions of ROMs to fix issues. Issues are less of a concern with the most popular classics because most of those haven't changed in years. But to avoid having to track multiple different versions of your ROMs, most people just keep their ROM sets updated as the emulator updates.

To understand how MAME works, look up the difference between merged and split ROM sets, and learn what a sample and a chd are and how they're used in conjunction with ROMs to deliver a playable game.

Reference image: <img src="https://user-images.githubusercontent.com/108900299/230745173-8be48509-2131-4dc7-b4da-efb96a4b2594.png" height="300">

!!! tip

    Refer to [https://docs.mamedev.org/usingmame/aboutromsets.html](https://docs.mamedev.org/usingmame/aboutromsets.html), for additional information.

---

### How to Configure Multiplayer



Multiplayer for MAME is configured out of the box, no additional configuration is needed.

You may need to re-arrange the controller order in Game Mode for your controllers to function as expected. See [How to Re-Arrange the Controller Order](../../controls-and-hotkeys/steamos/external-controllers.md#how-to-re-arrange-the-controller-order) for more information.

---

### How to Determine if a ROM Requires BIOS



Some ROMs for MAME may require BIOS to run. For this section, these ROMs will be split into either `System` or `Software` ROMs. To delineate between the two simply, `System` ROMs are typically arcade ROMs and `Software` ROMs are usually computers or video game consoles.

#### How to Determine if a System ROM Requires BIOS



1. In a folder of your choice, right click anywhere in the folder, and click `Open Terminal here`
2. Enter:
   - `flatpak run org.mamedev.MAME -listxml > mame.xml`
3. This command will create a `mame.xml` file in the folder you chose in Step 1
4. Right click `mame.xml`, click `Open with Kate` or a text editor of your choice
5. Search the file (either using `Ctrl` + `F` or by clicking `Edit` --> `Find`) and type in `isbios`
6. You will see a line that generally looks like the following:
   - `<machine name="MACHINENAME" sourcefile="PATH/FILENAME" isbios="yes">`
   - For example
     - `<machine name="neogeo" sourcefile="neogeo/neogeo.cpp" isbios="yes">`
7. Let's break this line down, using `neogeo` as an example:
   - `<machine name="neogeo" sourcefile="neogeo/neogeo.cpp" isbios="yes">`
     - `isbios="yes"` means BIOS are required for the Neo-Geo MV-6F
     - The `machine_name=` gives you the name of the BIOS file. BIOS files for `System` ROMs always have a `.zip` file extension. For `neogeo`, the bios will be `neogeo.zip`
     - The list of files below the `manufacturer` typically comprise the files in a merged `neogeo.zip` file. Using a merged `neogeo.zip` may take up extra space but guarantees you have the BIOS necessary to play any Neo-Geo MV-6F ROM
8. Place your BIOS in `Emulation/bios` or `Emulation/roms/arcade` (the latter is required if you are playing through EmulationStation-DE)

Recreating this file whenever MAME updates will get you the latest list of which System ROMs require BIOS.

#### How to Determine if a Software ROM Requires BIOS



1. Open [http://adb.arcadeitalia.net/default.php](http://adb.arcadeitalia.net/default.php)
2. Search for the name of the console or computer in the search box, respecting punctuation and hyphenation when possible
3. On the respective console or computer's page, scroll down to `Required Files`, and click `SHOW MAME REQUIRED FILES`
   - ![Game.com Example](../../assets/mame-required-bios-software-1.png)
4. Place the file(s) in the list in `Emulation/bios` or the matching ROM folder (the latter is required if you are playing through EmulationStation-DE)
   - For example, if you are playing `Game.com` through EmulationStation-DE, place `gamecom.zip` in `Emulation/roms/gamecom`

##### How to View Compatibility for Software ROMs



1. Open [http://adb.arcadeitalia.net/default.php](http://adb.arcadeitalia.net/default.php)
2. Click `SOFTWARE` on the left side
3. Search for your console or computer in the `SYSTEM` box and click `Search`
   - For example, Game.com: [http://adb.arcadeitalia.net/?search=mess&machine_name=gamecom%3B](http://adb.arcadeitalia.net/?search=mess&machine_name=gamecom%3B)
4. You will see a full list of the ROMs for that respective console or computer. The circle color in the top right of each box is the game's compatibility
   - Green: Supported
   - Yellow: Imperfect
     - Some pages may explain the specific issues affecting the game
   - Red: Not Supported

---

### How to Determine if a ROM Requires a CHD File



Game ROMs for MAME are primarily `.zip` files. Some of these games require additional files to run. These additional files are primarily `.chd` files.

To determine if your ROM requires a `.chd` file:

1. In Desktop Mode, open Konsole
2. Enter:
   - `flatpak run org.mamedev.MAME -listroms ROMSHORTNAME`
     - Typically, the short name of the ROM is the file name. For example, the file name for `Street Fighter III 3rd Strike` is `sfiii3.zip` and the short name is `sfiii3`
     - You can also use [http://adb.arcadeitalia.net/](http://adb.arcadeitalia.net/) to locate a MAME ROM's short name
3. You will get an output similar to below:
   `        ROMs required for driver "sfiii3".
        Name                                   Size Checksum
        sfiii3_euro.29f400.u2                524288 CRC(30bbf293) SHA1(f094c2eeaf4f6709060197aca371a4532346bf78)
        cap-33s-2                                   SHA1(5a090956fc6d68e496ac42854199059898f2fe16)
       `
4. The line without a file size or a CRC is the `.chd` file required. The line with a file size and a CRC is the file located within the zip file
   - For example, `sfiii3_euro.29f400.u2` is the file located in `sfiii3.zip` and `cap-33s-2` is the `.chd` file required to run `sfiii3.zip`
5. Create a subfolder matching the shortname in `Emulation/roms/arcade` and place the `.chd` file in the subfolder
   - For example, with `sfiii3`, create a `sfiii3` folder in `Emulation/roms/arcade` and place `cap-33s-2.chd` in `Emulation/roms/arcade/sfiii3`
   - Place `sfiii3.zip` directly in `Emulation/roms/arcade`

---

### How to Configure Controls on a Per Game Basis



1. While in game, press `STEAM` and `DPad Down`
2. Select `Input Settings`
3. Select `Input Settings (this system)`
4. Configure controls
5. To ensure your controls are saved, press `STEAM` and `DPad Left` to exit out of the game
   - If you press `STEAM` and use the `Exit game` button, your controls will not be saved
6. Your controls will be saved as a file to `home/deck/.mame/cfg/GAMESHORTNAME.cfg`
   - You may also share this configuration file with others

---

### How to Add Custom Bezels



1. Open `Emulation/storage/mame`
2. Copy bezel files, in .zip format, into this folder, named the same as the ROM.
3. Done.

!!! tip

    Use the Bezel Project to locate bezels for your MAME ROMs: [https://github.com/thebezelproject/BezelProject-Windows](https://github.com/thebezelproject/BezelProject-Windows)

---

### How to Enable Shaders/Scanlines in MAME (Standalone)



1. In Desktop Mode, open `/home/deck/.mame/mame.ini`
   - `~/.mame` is a hidden folder by default. In Dolphin (file manager), click the hamburger menu in the top right, click `Show Hidden Files` to see these folders.
2. Under the `OSD VIDEO OPTIONS` section, set `video` to `bgfx`
3. Under the `BGFX POST-PROCESSING OPTIONS` section, set `bgfx_screen_chains` to the shader of your choice
   - For example: `crt-geom-deluxe`
4. Save your changes to the file

!!! tip

    Other shader values can be found here: [https://docs.mamedev.org/advanced/bgfx.html](https://docs.mamedev.org/advanced/bgfx.html)

---

### How to Configure MAME to Work With EmulationStation-DE



EmuDeck installs both MAME (Standalone, installed as a flatpak), and RetroArch's MAME core.

In order to use MAME (Standalone), make sure your ROMs are in `Emulation/roms/arcade`.

In order to use MAME (Standalone) for EmulationStation-DE, make sure you are selecting `MAME [Standalone]` in the `Alternative Emulators` menu.

**Tutorial**

1. In EmulationStation-DE, press the `Start` button
2. Scroll down and select `Other Settings`
3. Select `Alternative Emulators`
4. Scroll down to `Arcade` and select `MAME [Standalone]`

---

### How to Roll Back MAME to an Older Version



If you do not have access to a mouse and keyboard for the below section, use `L2` to right click and `R2` to left click. Alternatively, remote into your Steam Deck using one of the methods found in the FAQ, [How do I remotely control my Steam Deck?](../../frequently-asked-questions/steamos/index.md#how-do-i-remotely-control-my-steam-deck).

1. In Desktop Mode, open `Konsole`
2. To see a list of prior versions of the emulator, type:
   - `flatpak remote-info --log flathub org.mamedev.MAME`
3. If Konsole prompts you to select `system` or `user`, enter `2` to select `user`
4. Konsole will list a list of previous versions for the flatpak. The important line for each version is the `Commit: ` line. The `Commit: ` line will have a long accompanying alphanumeric string (the “commit” code). Copy the string for the version you want to downgrade to.
   - Using Citra as an example:
     - ![How to Roll Back Flatpaks: 1](../../assets/how-to-roll-back-flatpaks-1.png)
5. To downgrade to the version you want:
   - `flatpak update --commit=put_commit_code_here org.mamedev.MAME`
   - Replace `put_commit_code_here` with the actual code you located in Step 2.
     - Using Citra as an example:
       - ![How to Roll Back Flatpaks: 2](../../assets/how-to-roll-back-flatpaks-2.png)

If the above steps did not work and you are getting an error message along the lines of `Flatpak not installed`, your Flatpak is likely installed at the system level instead. Select one of the below solutions:

Solution 1: Open the EmuDeck application, click the `Manage Emulators` page, select the emulator in question, and click `Reinstall / Update`.

Solution 2: Add `sudo` in front of the commands written in Step 2 and Step 5. In Step 2, write `sudo flatpak remote-info --log flathub org.mamedev.MAME` and in Step 5, write `sudo flatpak update --commit=put_commit_code_here org.mamedev.MAME`.

---

### How to Configure Language Settings



#### UI

1. In Desktop Mode, open MAME
2. At the bottom, click `General Settings`
3. Click `Customize UI`
4. Click `Language`, select your preferred language in the drop-down menu

---

### How to Use Cheats



1. Download the latest cheat package from [https://www.mamecheat.co.uk/](https://www.mamecheat.co.uk/). Click the `XML/JSON Cheat Collection for MAME 0.###` at the top to download the latest cheat package
   - `###` matches the MAME version of the cheat package which may vary depending on when you visit the site
2. Extract `cheat###.zip` to a folder of your choice
   - `###` matches the MAME version of the cheat package which may vary depending on when you visit the site
3. Move `cheat.7z` from the extracted folder to `Emulation/storage/mame/cheat`
4. Open MAME without a game loaded, click `General Settings`, `Miscellaneous Options`, toggle `Cheats` on, back out of this menu, click `Save Settings`
5. While in game, press `Select` + `R3` to open the Quick Menu, click `Cheat Options`, enable cheat(s)

---

### How to Configure Light Gun Games



1. In Game Mode, single click the game you would like to change the Steam Input Profile for, and click the `Controller Icon` on the right of the screen. Click the layout (whichever name it is currently set to) at the top
2. Click the `Templates` tab
3. Select the `EmuDeck - Steam Deck Light Gun Controls` profile
4. Light gun controls will now be configured for this game

{{ read_csv('emudeck-steam-deck-light-gun-controls.csv') }}

---
