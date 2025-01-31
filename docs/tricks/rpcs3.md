# <img src="/assets/emulators/rpcs3.png" alt="EmuDeck guide" width="80" style="vertical-align: middle"> RPCS3 Tips and Tricks

[TOC]

---

### How to Configure RPCS3 to Work With ES-DE and Pegasus



## AppImage

1. In `Desktop Mode`, open RPCS3
2. Skip this step if you have already added your games to RPCS3:
   - Either:
     - In the top left click, `File`, click `Add Games`, locate your game
     - In the top left click, `File`, click `Install Packages/Raps/Edats`, and install your PKG
     - For more information, read the [File Formats](#rpcs3-file-formats) section
3. Right click your game, click `Create Shortcut`, click `Create Desktop Shortcut`
4. On your desktop, you should see an icon for your game. Move this icon to `Emulation/roms/ps3`
   - If your desktop shortcut contains special icons any special symbols (Ex: the copyright symbol, `©`), rename the desktop file to remove these symbols.
     - For example, rename `God Of War® Collection.desktop` to `God Of War Collection.desktop`, removing the `©` after `War`
5. (Optional) If the desktop file is opening RPCS3 instead of the game:
   - In Desktop Mode, right click the desktop file
   - Click `Properties`
   - On the `General` tab, click `Change` to the right of the `Open With` line
   - Under `Application Preference Order`, click `RPCS3`
   - Click `Remove` on the right
   - Click `Apply` in the bottom left and click `OK`
   - The desktop file will not work in Desktop Mode, but will launch the game directly either through a terminal or through ES-DE
6. Your game should now show up in and launch directly from ES-DE and Pegasus

If you get an `Invalid file or folder` error message, you will need to change the `Alternative Emulator` in ES-DE for PlayStation 3 to `RPCS3 Shortcut [Standalone]`.

You may also do this on a per-game basis if you are using a mix of folders and PKGs. On a game, press the `select ` button, scroll down and select `EDIT THIS GAME'S METADATA`, scroll down and select `ALTERNATIVE EMULATOR`, select PS3 and select the corresponding format.

Refer to [https://gitlab.com/es-de/emulationstation-de/-/blob/master/USERGUIDE.md#sony-playstation-3](https://gitlab.com/es-de/emulationstation-de/-/blob/master/USERGUIDE.md#sony-playstation-3), for additional information.

## Flatpak

**These are legacy instructions for the Flatpak installation from Discover. If you would like to use the AppImage, see [Why did EmuDeck switch to the AppImage?](Why did EmuDeck switch to the AppImage?) for instructions.**

1. In `Desktop Mode`, open RPCS3
2. Skip this step if you have already added your games to RPCS3:
   - Either:
     - In the top left click, `File`, click `Add Games`, locate your game
     - In the top left click, `File`, click `Install Packages/Raps/Edats`, and install your PKG
     - For more information, read the [File Formats](#rpcs3-file-formats) section
3. Right click your game, click `Create Shortcut`, click `Create Desktop Shortcut`
4. On your desktop, you should see an icon for your game. Move this icon to `Emulation/roms/ps3`
5. Right click the shortcut, click `Open with Kate` or a text editor of your choice
6. Edit the **beginning** of the `Exec=` line using the following template:
   - Original Line: ``Exec="/app/bin/rpcs3" --no-gui`
   - Updated Line: `Exec="/usr/bin/flatpak" run net.rpcs3.RPCS3 --no-gui`
     - Replace `"/app/bin/rpcs3" --no-gui` with `"/usr/bin/flatpak" run net.rpcs3.RPCS3 --no-gui`
   - **Do not** edit anything on the line after `--no-gui`
7. Example, using Demon Souls:
   - **Original Line:** `Exec="/app/bin/rpcs3" --no-gui "%%RPCS3_GAMEID%%:BLUS30443"`
     - ![Original Line](../../assets/how-to-configure-rpcs3-with-emulationstation-de-original-line.png)
   - **Updated Line:** `Exec="/usr/bin/flatpak" run net.rpcs3.RPCS3 --no-gui "%RPCS3_GAMEID%:BLUS30443"`
8. Save and close out of the desktop file
9. (Optional) If the desktop file is opening RPCS3 instead of the game:
   - In Desktop Mode, right click the desktop file
   - Click `Properties`
   - On the `General` tab, click `Change` to the right of the `Open With` line
   - Under `Application Preference Order`, click `RPCS3`
   - Click `Remove` on the right
   - Click `Apply` in the bottom left and click `OK`
   - The desktop file will not work in Desktop Mode, but will launch the game directly either through a terminal or through ES-DE and Pegasus
10. Your game should now show up in and launch directly from ES-DE and Pegasus

If you get an `Invalid file or folder` error message, you will need to change the `Alternative Emulator` in ES-DE for PlayStation 3 to `RPCS3 Shortcut [Standalone]`.

You may also do this on a per-game basis if you are using a mix of folders and PKGs. On a game, press the `select` button, scroll down and select `EDIT THIS GAME'S METADATA`, scroll down and select `ALTERNATIVE EMULATOR`, select PS3 and select the corresponding format.

Refer to [https://gitlab.com/es-de/emulationstation-de/-/blob/master/USERGUIDE.md#sony-playstation-3](https://gitlab.com/es-de/emulationstation-de/-/blob/master/USERGUIDE.md#sony-playstation-3), for additional information.

---

### How to Configure Multiplayer



RPCS3 comes with a nifty auto-map feature that makes setting up multiplayer a breeze. To set up multiplayer, you simply need to enable the additional ports.

**Note:** If you are in Desktop Mode, make sure that Steam is open.

1. Open RPCS3
2. Open the `Pads` menu in the `Settings`
3. For each controller you are using for Player 2, 3, 4, etc, click the respective tab
   - You do not need to adjust any settings for Player 1
4. Under `Handlers`, select `SDL` for each player you are enabling
5. Under `Devices`
   - Player 2: `Steam Virtual Gamepad 2`
   - Player 3: `Steam Virtual Gamepad 3`
   - Player 4: `Steam Virtual Gamepad 4`
   - Player 5: `Steam Virtual Gamepad 5`
   - Player 6: `Steam Virtual Gamepad 6`
   - Player 7: `Steam Virtual Gamepad 7`
6. Using `Player 2` as an example:
   - On the `Player 2` configuration screen, after you have selected the appropriate `Device` and `Handler`, click `Refresh` to the right of `Handler`
7. After you are finished enabling any additional players, click `Save` and you may open your game either directly as a shortcut in Steam or through ES-DE and Pegasus
8. (Optional) You may need to re-arrange the controller order in Game Mode for your controllers to function as expected. See [How to Re-Arrange the Controller Order](../../controls-and-hotkeys/steamos/external-controllers.md#how-to-re-arrange-the-controller-order) to learn how

---

### Special Game Configurations



#### RPCS3 Wiki

Some games may require additional setup, needing mods or alteration of settings. The [RPCS3 Compatability List](https://rpcs3.net/compatibility) can be used to check for these. Simply search for the name of the game and click the hyperlinked name to view the wiki page for that game and see if there are any recommended or required settings changes.

#### EmuDeck Community Creations

Use the EmuDeck [Community Game Configurations](../../community-creations/steamos/community-game-configurations.md#rpcs3) page to submit or view special game configurations.

---

### How to Set up the Motion Sensor with External Controllers



The PlayStation 3 controller, or the DualShock 3 notably had "Sixaxis". Sixaxis refers to the motion sensor used in a handful of games. One of the more popular games that utilized Sixaxis was Folklore. For a full list of games, see [https://www.giantbomb.com/sixaxis-support/3015-5310/games/](https://www.giantbomb.com/sixaxis-support/3015-5310/games/).

RPCS3 has implemented support to allow emulating the Sixaxis through evdev, which exposes the gyro in a large variety of modern controllers (including the Nintendo Switch Pro Controller, 8BitDo Ultimate Controller, and the DualSense).

At this time, the Steam Deck gyro **cannot** be used. But if you own one of these controllers, you may emulate the Sixaxis through RPCS3.

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
   - You may also connect an external keyboard and mouse
3. Click the bluetooth icon in the bottom right of your taskbar and connect your controller
4. Click the Steam icon in the bottom left of the taskbar and open `RPCS3`
5. Click `Pads` at the top
6. Under the `Player 1` tab, click the Dropdown box below `Devices` and select your controller
   - To switch back to the default controller layout, make sure `Steam` is open and select `Steam Virtual Gamepad 1`
7. Click `Save`, and exit out of RPCS3

#### Game Mode

1. In Game Mode, connect your controller
2. Select your PlayStation 3 game
3. On the `Play` screen, select the `Controller` icon to the right of the screen
4. Select your controller tab at the top
5. Click `Reorder Controllers` and move your external controller to the top
6. Click the `Gear` icon to the right, and click `Disable Steam Input`
   - You may need to restart first for this setting to properly apply
7. Your controller's gyro will now work for this selected game, repeat as needed for your other games

For a video, see below:

<figure class="video_container">
  <video controls="true" allowfullscreen="true">
    <source src="/videos/how-to-disable-steam-input.mp4" type="video/mp4">
  </video>
</figure>

#### Post-Configuration

To restore the default Steam Deck controls:

1. Open RPCS3
2. Click `Pads` at the top
3. Under the `Player 1` tab, click the Dropdown box below `Devices` and select `Steam Virtual Gamepad 1`
4. Select `SDL` under `Handlers`
5. Click `Save`, and exit out of RPCS3

(Optional) To restore Steam Input:

1. Select your PlayStation 3 game
2. On the `Play` screen, select the `Controller` icon to the right of the screen
   <img src="https://github.com/dragoonDorise/EmuDeck/assets/108900299/468d63e3-534c-4270-ac61-06e167d6df48" height="300">
3. Select your controller tab at the top
   <img src="https://github.com/dragoonDorise/EmuDeck/assets/108900299/b51a1405-9cdf-4ba3-bebf-db817f057f63" height="300">
4. Click the `Gear` icon to the right, and click `Enable Steam Input`
   - You may need to restart first for this setting to properly apply
5. The controls will be reverted to Steam Input and the Steam Deck controls will be restored

---

### How to Roll Back RPCS3 to an Older Version



#### AppImage

##### Introduction

Your ROMs launch using a script created by EmuDeck, `rpcs3.sh` in `~/Emulation/tools/launchers`.

!!! info "Emulation Directory"
`~/Emulation` refers to either your `home` directory or SD Card/removable media depending on your installation location.

The script launches the corresponding emulator in `/home/deck/Applications` and **specifically looks** for two traits:

- The most recently downloaded version of the emulator in `/home/deck/Applications`, based on the file/release date.
- The emulator name at the beginning of the file. Anything after the emulator name is ignored.
  - For example, if the latest version of the emulator is `1351` and you would like to downgrade to `1349`. When you download version `1349`, you could rename it to `EMULATORNAME-1349.AppImage`, and EmuDeck's script will ignore the `-1349` in the file name, allowing you to record which versions of the emulator you are using through the file name.

##### How to Roll Back RPCS3

1. Download the version of the emulator you would like to use from RPCS3's Builds page: [https://rpcs3.net/compatibility?b](https://rpcs3.net/compatibility?b)
2. Move the downloaded emulator from Step 1 to `/home/deck/Applications`
3. **(Optional)** Rename or delete the original emulator file
4. Right click the newly downloaded emulator, click `Properties`, click `Permissions`, check `Is executable`
5. Your games will now launch using the version of the emulator you downloaded

##### Flatpak

**These are legacy instructions for the Flatpak installation from Discover. If you would like to use the AppImage, see [Why did EmuDeck switch to the AppImage?](Why did EmuDeck switch to the AppImage?) for instructions.**

If you do not have access to a mouse and keyboard for the below section, use `L2` to right click and `R2` to left click. Alternatively, remote into your Steam Deck using one of the methods found in the FAQ, [How do I remotely control my Steam Deck?](../../frequently-asked-questions/steamos/index.md#how-do-i-remotely-control-my-steam-deck).

1. In Desktop Mode, open `Konsole`
2. To see a list of prior versions of the emulator, type:
   - `flatpak remote-info --log flathub net.rpcs3.RPCS3`
3. If Konsole prompts you to select `system` or `user`, enter `2` to select `user`
4. Konsole will list a list of previous versions for the flatpak. The important line for each version is the `Commit: ` line. The `Commit: ` line will have a long accompanying alphanumeric string (the “commit” code). Copy the string for the version you want to downgrade to.
   - Using Citra as an example:
     - ![How to Roll Back Flatpaks: 1](../../assets/how-to-roll-back-flatpaks-1.png)
5. To downgrade to the version you want:
   - `flatpak update --commit=put_commit_code_here net.rpcs3.RPCS3`
   - Replace `put_commit_code_here` with the actual code you located in Step 2.
     - Using Citra as an example:
       - ![How to Roll Back Flatpaks: 2](../../assets/how-to-roll-back-flatpaks-2.png)

If the above steps did not work and you are getting an error message along the lines of `Flatpak not installed`, your Flatpak is likely installed at the system level instead. Select one of the below solutions:

Solution 1: Open the EmuDeck application, click the `Manage Emulators` page, select the emulator in question, and click `Reinstall / Update`.

Solution 2: Add `sudo` in front of the commands written in Step 2 and Step 5. In Step 2, write `sudo flatpak remote-info --log flathub net.rpcs3.RPCS3` and in Step 5, write `sudo flatpak update --commit=put_commit_code_here net.rpcs3.RPCS3`.

---

### How to Configure Language Settings



#### In-Game

1. In Desktop Mode, open RPCS3
2. At the top, click `Configuration`, click `System`
3. Below `Console Language`, select your preferred language in the drop-down menu

---
