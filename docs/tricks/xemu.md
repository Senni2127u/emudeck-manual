# <img src="/assets/emulators/xemu.png" alt="EmuDeck guide" width="80" style="vertical-align: middle"> Xemu Tips and Tricks

[TOC]

---

### How to Convert ROMs to XISO Format



#### List of Methods

- [Method 1: Use the xiso Website (Steam Deck)](#method-1-use-the-xiso-website-steam-deck)
- [Method 2: Use XDVDMulleter (Windows)](#method-2-use-xdvdmulleter-windows)
- [Method 3: extract-iso (Windows)](#method-3-extract-iso-windows)
- [Method 4: extract-iso (Linux)](#method-4-extract-iso-linux)
- [Method 5: extract-iso (Mac)](#method-5-extract-iso-mac)
- [Method 6: dd](#method-6-dd-linux)

---

##### Method 1: Use the xiso Website (Steam Deck)



Instructions provided on website.

**Link:** [https://xiso.antangelo.com/](https://xiso.antangelo.com/)

**Note:**

- This website is still in beta
- If it does not work on Firefox, use Chrome or Edge instead

---

##### Method 2: Use XDVDMulleter (Windows)



Link: [https://archive.org/details/xdvdmulleterv10.2beta](https://archive.org/details/xdvdmulleterv10.2beta)

![1](https://user-images.githubusercontent.com/108900299/194170038-5b4f69ed-853c-4332-b9c5-00b43679b449.png)
![2](https://user-images.githubusercontent.com/108900299/194170057-95e650e2-7dfb-4dcc-99b8-f4e6b5aaf689.png)
![3](https://user-images.githubusercontent.com/108900299/194170067-4062edeb-cafc-4606-88db-7f091030606e.png)

---

##### Method 3: extract-iso (Windows)



Link: [https://github.com/XboxDev/extract-xiso](https://github.com/XboxDev/extract-xiso)

**Instructions**

1. Go to the releases tab: [https://github.com/XboxDev/extract-xiso/releases/tag/build-202204252159](https://archive.org/details/xdvdmulleterv10.2beta)
2. Download the release .ZIP
3. Extract it somewhere on your computer
4. Put the untrimmed Xbox .ISO in the same directory
5. Rename the .ISO to something without spaces like `game-redump.iso` (doesn't have to be this exact name)
6. Open command prompt on your computer
7. Navigate to the directory containing the .EXE and your .ISO
8. Run `extract-xiso -r game-redump.iso`

Xemu's Tutorial: [https://xemu.app/docs/disc-images/](https://xemu.app/docs/disc-images/)

---

##### Method 4: extract-iso (Linux)



Note: Cannot be _built_ on the Steam Deck, but can be built elsewhere and copied. Then, it is usable on Steam Deck.

1.  Enter these commands in your terminal

         # Install dependencies
         # Example for Arch:
         sudo pacman -Syu --needed base-devel cmake

         # Clone Repo
         git clone https://github.com/XboxDev/extract-xiso.git

         # cd into directory
         cd extract-xiso

         # Create working directory
         mkdir build
         cd build

         # Build project
         cmake ..
         make

2.  Put the untrimmed Xbox .ISO in the same directory
3.  Rename the .ISO to something without spaces like `game-redump.iso` (doesn't have to be this exact name)
4.  Navigate to the directory containing your .ISO
5.  Run `extract-xiso -r game-redump.iso`

---

##### Method 5: extract-iso (Mac)



1. ⁠Open terminal
2. In terminal type the following: `Xcode-select --install`
3. Click allow on the Pop-up
4. Navigate to `extract-xiso`, cd `the/path/to/extract-xiso`
5. Type `make`
6. Then type the following: `sudo chmod +x extract-iso`
7. Finally run the executable: `./extract-xiso name\of\game.iso`

---

##### Method 6: dd (Linux)



**Note:** May not work on Steam Deck, needs testing.

Refer to Xemu's wiki for instructions, [https://xemu.app/docs/disc-images/#about-redump-isos](https://xemu.app/docs/disc-images/#about-redump-isos.)

---

### How to Configure Multiplayer



Xemu comes with a nifty auto-map feature that makes setting up multiplayer a breeze. To set up multiplayer, you simply need to enable the additional ports.

1. Open Xemu
2. Open the `Input` settings
3. For each controller you are using for Player 2, 3, and 4, click the respective tab
   - You do not need to adjust any settings for Player 1
4. In the drop-down menu
   - Player 2: `Steam Virtual Gamepad 2`
   - Player 3: `Steam Virtual Gamepad 3`
   - Player 4: `Steam Virtual Gamepad 4`
5. After you are finished enabling any additional players, exit out of Xemu and you may open your game either directly as a shortcut in Steam or through ES-DE
6. (Optional) You may need to re-arrange the controller order in Game Mode for your controllers to function as expected. See [How to Re-Arrange the Controller Order](../../controls-and-hotkeys/steamos/external-controllers.md#how-to-re-arrange-the-controller-order) to learn how

---

### How to Apply Zink



#### Preface

On the Steam Deck, some Xbox game graphics will not render properly. Applying Zink can fix these graphical issues.

However, Zink can also cause performance hits in certain games. Apply it on a per-game basis and keep in mind that if performance is degraded, it may be due to Zink.

You can read more about the issue here: [https://github.com/xemu-project/xemu/issues/1279#issuecomment-1381015271](https://github.com/xemu-project/xemu/issues/1279#issuecomment-1381015271).

Read one of the below sections to learn how to apply Zink to your Xbox games.

**Practical Uses of Zink**

- Fixes graphical issues
- Improves performance in some games (may worsen in others)
- Fixes black screen issues in some games

#### How to Apply Zink to ES-DE Games



1. In Desktop Mode, open the `Emulation/roms/xbox` folder
2. Right click anywhere in the folder, click `Create New --> Text File`
   <img src="https://user-images.githubusercontent.com/108900299/226739494-0e7b44c7-0fcf-4f9b-820a-8fa3351cfcfc.png" height="300">
3. Match the name of the text file to the game you are applying Zink to and change the file extension to `.esprefix`
   - For example:
     - ROM Name: `Conker - Live & Reloaded.iso`
     - New text file name: `Conker - Live & Reloaded.esprefix`
   <img src="https://user-images.githubusercontent.com/108900299/226740001-1738684d-854c-4466-86f3-96e14ac1bfb0.png" height="300">
4. Open the newly created text file in Kate or a text editor of your choice
5. On a single line, write:
   - `__GLX_VENDOR_LIBRARY_NAME=mesa MESA_LOADER_DRIVER_OVERRIDE=zink GALLIUM_DRIVER=zink`
   - Example:
     <img src="https://user-images.githubusercontent.com/108900299/226754331-28689940-10ef-42b5-9164-4bc58188ea68.png" height="300">
6. Zink will now be applied to this specific game in ES-DE, repeat for each game you would like to apply Zink

#### How to Apply Zink to Pegasus Games

1.  In Desktop Mode, open the `Emulation/roms/xbox/roms` folder
2.  Right click `metadata.txt`, click `Open with Kate` or a text editor of your choice
3.  At the bottom of the text file, add a new section using the following format:

        game: GAMENAME
        file: FILENAME
        launch: /PATH/TO/xemu.sh "{file.path}" __GLX_VENDOR_LIBRARY_NAME=mesa MESA_LOADER_DRIVER_OVERRIDE=zink GALLIUM_DRIVER=zink

4.  Replace GAMENAME with the name of the game
    - For example:
      - `Conker: Live & Reloaded`
5.  Replace FILENAME with the file name
    - For example:
      - `Conker: Live & Reloaded.iso`
6.  Edit `/PATH/TO` with the path to `xemu.sh`, the path for `xemu.sh` will be at the top of the `metadata.txt` file, you may copy it here
7.  Save and exit out of the file
8.  Zink will now be applied to this specific game in Pegasus, repeat for each game you would like to apply Zink

#### How to Apply Zink to Steam ROM Manager Shortcuts



1. In Desktop Mode, open Steam
2. Select an Xbox Game shortcut in Steam
3. Click the `Gear` icon
   <img src="https://user-images.githubusercontent.com/108900299/226738898-c724328a-b91c-42d8-91d3-4109998b8212.png" height="300">
4. Click `Properties`
5. In the `Launch Options` box, enter: `__GLX_VENDOR_LIBRARY_NAME=mesa MESA_LOADER_DRIVER_OVERRIDE=zink GALLIUM_DRIVER=zink %command%`
   <img src="https://user-images.githubusercontent.com/108900299/226739203-c14b2c57-3029-4f87-baa3-2fa9d0af8bef.png" height="300">
6. Zink will now be applied to this specific game's Steam shortcut, repeat for each game you would like to apply Zink

---

### vs_position_always_invariant=true



For more information on what `vs_position_always_invariant=true` is, see [https://gitlab.freedesktop.org/mesa/mesa/-/commit/9b577f2a887968483b88b629673d3f9904a179ff](https://gitlab.freedesktop.org/mesa/mesa/-/commit/9b577f2a887968483b88b629673d3f9904a179ff).

Setting `vs_position_always_invariant=true` for Xemu games can be considered an alternative option to the [How to Apply Zink](#how-to-apply-zink) section. Zink may cause performance issues or graphical issues. If that is the case, you can try the steps in this section. However, applying `vs_position_always_invariant=true` may also cause its own set of performance or graphical issues.

**Practical Uses of `vs_position_always_invariant=true`**

- Fixes black screen issues
  - Games with black screen issues (Not an exhaustive list)
    - Burnout 3 and Phantom Dust

Read one of the below sections to learn how to apply Zink to your Xbox games.

#### How to Apply vs_position_always_invariant=true to ES-DE Games

1. In Desktop Mode, open the `Emulation/roms/xbox` folder
2. Right click anywhere in the folder, click `Create New --> Text File`
   <img src="https://user-images.githubusercontent.com/108900299/226739494-0e7b44c7-0fcf-4f9b-820a-8fa3351cfcfc.png" height="300">
3. Match the name of the text file to the game you are applying `vs_position_always_invariant=true` to and change the file extension to `.esprefix`
   - For example:
     - ROM Name: `Conker - Live & Reloaded.iso`
     - New text file name: `Conker - Live & Reloaded.esprefix`
   <img src="https://user-images.githubusercontent.com/108900299/226740001-1738684d-854c-4466-86f3-96e14ac1bfb0.png" height="300">
4. Open the newly created text file in Kate or a text editor of your choice
5. On a single line, write:
   - `vs_position_always_invariant=true`
6. `vs_position_always_invariant=true` will now be applied to this specific game in ES-DE, repeat for each game you would like to apply `vs_position_always_invariant=true`

#### How to Apply vs_position_always_invariant=true to Pegasus Games

1.  In Desktop Mode, open the `Emulation/roms/xbox/roms` folder
2.  Right click `metadata.txt`, click `Open with Kate` or a text editor of your choice
3.  At the bottom of the text file, add a new section using the following format:

        game: GAMENAME
        file: FILENAME
        launch: /PATH/TO/xemu.sh "{file.path}" vs_position_always_invariant=true

4.  Replace GAMENAME with the name of the game
    - For example:
      - `Conker: Live & Reloaded`
5.  Replace FILENAME with the file name
    - For example:
      - `Conker: Live & Reloaded.iso`
6.  Edit `/PATH/TO` with the path to `xemu.sh`, the path for `xemu.sh` will be at the top of the `metadata.txt` file, you may copy it here
7.  Save and exit out of the file
8.  `vs_position_always_invariant=true` will now be applied to this specific game in Pegasus

#### How to Apply vs_position_always_invariant=true to Steam ROM Manager Shortcuts

1. In Desktop Mode, open Steam
2. Select an Xbox Game shortcut in Steam
3. Click the `Gear` icon
   <img src="https://user-images.githubusercontent.com/108900299/226738898-c724328a-b91c-42d8-91d3-4109998b8212.png" height="300">
4. Click `Properties`
5. In the `Launch Options` box, enter: `vs_position_always_invariant=true %command%`
6. `vs_position_always_invariant=true` will now be applied to this specific game's Steam shortcut, repeat for each game you would like to apply `vs_position_always_invariant=true`

---

### How to Access Saves



Your save files are located here: `Emulation/storage/xemu/xbox_hdd.qcow2`

**How to Access Saves**

Download [https://github.com/Ryzee119/LithiumX/releases](https://github.com/Ryzee119/LithiumX/releases), extract the zip file, and launch the ISO in Xemu.

Follow the instructions here: [https://xemu.app/docs/ftp/](https://xemu.app/docs/ftp/), to access the saves in the `xbox_hdd.qcow2` file.

---

### How to Roll Back Xemu to an Older Version



If you do not have access to a mouse and keyboard for the below section, use `L2` to right click and `R2` to left click. Alternatively, remote into your Steam Deck using one of the methods found in the FAQ, [How do I remotely control my Steam Deck?](../../frequently-asked-questions/steamos/index.md#how-do-i-remotely-control-my-steam-deck).

1. In Desktop Mode, open `Konsole`
2. To see a list of prior versions of the emulator, type:
   - `flatpak remote-info --log flathub app.xemu.xemu`
3. If Konsole prompts you to select `system` or `user`, enter `2` to select `user`
4. Konsole will list a list of previous versions for the flatpak. The important line for each version is the `Commit: ` line. The `Commit: ` line will have a long accompanying alphanumeric string (the “commit” code). Copy the string for the version you want to downgrade to.
   - Using Citra as an example:
     - ![How to Roll Back Flatpaks: 1](../../assets/how-to-roll-back-flatpaks-1.png)
5. To downgrade to the version you want:
   - `flatpak update --commit=put_commit_code_here app.xemu.xemu`
   - Replace `put_commit_code_here` with the actual code you located in Step 2.
     - Using Citra as an example:
       - ![How to Roll Back Flatpaks: 2](../../assets/how-to-roll-back-flatpaks-2.png)

If the above steps did not work and you are getting an error message along the lines of `Flatpak not installed`, your Flatpak is likely installed at the system level instead. Select one of the below solutions:

Solution 1: Open the EmuDeck application, click the `Manage Emulators` page, select the emulator in question, and click `Reinstall / Update`.

Solution 2: Add `sudo` in front of the commands written in Step 2 and Step 5. In Step 2, write `sudo flatpak remote-info --log flathub app.xemu.xemu` and in Step 5, write `sudo flatpak update --commit=put_commit_code_here app.xemu.xemu`.

---

### How to Configure Language Settings



#### In-Game

Download and set up XboxEepromEditor. For instructions, see [How to Set Up XboxEepromEditor](../../community-creations/steamos/tools-and-guides.md#how-to-set-up-xboxeepromeditor).

1. Open XboxEepromEditor
2. In the top left, click `File`, `Open`
3. Click the `/` and navigate to your `Emulation/storage/xemu` folder
   - If your EmuDeck install is on an SD Card, your path will typically begin with `/run/media...`
   - If your EmuDeck install is on your internal SSD, your path will typically begin with `/home/deck..`
4. Select the `eeprom.bin` file
5. Under the `Security` tab, select your preferred region
   - Some regions may have more language options than others
6. Under the `General` tab, select your preferred language
7. After you have made your changes, click `File`, click `Save As`
8. In the `File Name` box, type `eeprom.bin`
9. Click the `/` and navigate to your `Emulation/storage/xemu` folder
   - If your EmuDeck install is on an SD Card, your path will typically begin with `/run/media...`
   - If your EmuDeck install is on your internal SSD, your path will typically begin with `/home/deck..`
10. Click `Save` and click `Yes` on the `File already exists, do you want to replace it?` prompt
11. Your preferred language settings will now be applied in Xemu

---
