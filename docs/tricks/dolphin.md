# <img src="/assets/emulators/dolphin.png" alt="EmuDeck guide" width="80" style="vertical-align: middle"> Dolphin Tips and Tricks

[TOC]

---

### How to Verify ROMs

[Back to the Top](#dolphin-table-of-contents)

If you have a ROM that is not launching, you can verify your ROM directly in Dolphin. Verifying your ROM confirms whether you have a good dump or a bad dump. If you have a bad dump, your issue may be that your ROM either transferred incorrectly or that you have a bad dump.

If your ROM transferred incorrectly, see [How to Transfer Files to a Steam Deck](../../file-management/steamos/file-management.md#how-to-transfer-files-to-a-steam-deck) for a few methods.

If you have a bad dump, re-dump your GameCube or Wii ROM, following Dolphin's guide. For the dumping guide, see [https://dolphin-emu.org/docs/guides/ripping-games/](https://dolphin-emu.org/docs/guides/ripping-games/).

If you have a good dump, your issue lies elsewhere. Make sure Dolphin is up to date. If neither of these resolve your issue, make sure to either check Google or retrieve a log so you can share it with the Dolphin team.

#### How to Verify ROMs

1. In Desktop Mode, open the Dolphin emulator
2. Right click a game
3. Click `Properties`
4. Click the `Verify` tab at the top
5. Click `Verify Integrity` at the bottom
6. In the text box in the middle of the screen, you will see a message stating if your ROM is a good or a bad dump

---

### How to Configure Gyro

[Back to the Top](#dolphin-table-of-contents)

Gyro for Dolphin requires SteamDeckGyroDSU. SteamDeckGyroDSU can be installed via EmuDeck, or it can be installed manually.

Visit [SteamDeckGyroDSU](../../emudeck-application/steamos/emudeck-application-101.md#steamdeckgyrodsu) to learn how to install and utilize SteamDeckGyroDSU.

**IMPORTANT**

Gyro for Dolphin is not mapped out of the box. You will need to open the Dolphin emulator and configure gyro controls after installing SteamDeckGyroDSU.

After installing SteamDeckGyroDSU, you may either choose to create your own profile in Dolphin or you may choose to download a community created profile from the [Community Creations](../../community-creations/steamos/community-creations.md) page.

Select **one** of the two options below.

#### Option 1: Downloading a Community Creations profile

Visit the [Community Creations](../../community-creations/steamos/community-creations.md) page. You may want to start with the [How to Download Dolphin Profiles](../../community-creations/steamos/community-creations.md#how-to-download-dolphin-profiles) section.

#### Option 2: Creating your own profile

If you are choosing to create your own profile:

1. Install and configure [SteamDeckGyroDSU](../../emudeck-application/steamos/emudeck-application-101.md#steamdeckgyrodsu)
2. Add the Dolphin emulator to Steam
   - You may add the Dolphin emulator to Steam by using the `Emulators` parser in Steam ROM Manager
3. In Game Mode, enable gyro for the Dolphin emulator
   - For instructions, see [SteamDeckGyroDSU](../../emudeck-application/steamos/emudeck-application-101.md#steamdeckgyrodsu)
4. In Game Mode, open the Dolphin emulator
5. Open the `Controllers` menu
6. Select `Configure` to the right of `Wii Remote 1`
   - Make sure `Wii Remote 1` is set to `Emulated Wii Remote`
7. Make sure `SDL/0/Virtual Steam Gamepad 1` is set in the top left
8. Select the `Motion Input` tab
9. Hover over any of the buttons under the `Accelerometer` or `Gyroscope` sections and press `STEAM` + `L2`
10. Make sure `DSUClient/0/steamdeckgyro` is selected in the drop-down menu at the top
11. Scroll down to the bottom of the list until you see `Accel` and `Gyro` direction inputs
12. Select the matching input to the button you clicked in Step 7
13. Press `Clear` in the bottom right
14. Press `Select` in the top right
    - ![Dolphin Gyro Example 1](../../assets/dolphin-gyro.png)
15. Press `OK` in the bottom right
16. Repeat for each button under the `Accelerometer` and `Gyroscope` sections
17. (Optional) To use the Steam Deck gyro as a pointer (moving the Steam Deck itself), check `Enable` under the Pointer section on the left on the `Motion Input` tab
    - Consider clicking `Recenter` and tinkering with the settings here to calibrate the pointer
18. After you are finished, give your profile a name in the top right and save it as a new profile
19. Refer to the [Dolphin Hotkeys](#dolphin-hotkeys) to learn how to switch profiles mid-game

**Note:** If you are having issues with the gyro pointer/cursor not appearing or behaving erratically, you may also want to consider disabling `Auto-hide` under the `Point` section on the `Motion simulation tab`.

For more information, read Dolphin's wiki page on gyro: [https://wiki.dolphin-emu.org/index.php?title=Motion_evdev](https://wiki.dolphin-emu.org/index.php?title=Motion_evdev).

---

### How to Configure Gyro With External Controllers

[Back to the Top](#dolphin-table-of-contents)

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
4. Open Dolphin
5. Open the `Controllers` menu
6. Select `Configure` to the right of `Wii Remote 1`
   - Make sure `Wii Remote 1` is set to `Emulated Wii Remote`
7. On the `Profile` drop-down, select `Wii_base_nunchuck_with_touchpad` if you are using a Nunchuk or `Wii_no_attachment_with_touchpad` if you are not using a Nunchuk
8. Under `Device`, select `SDL/0/yourexternalcontrollername`
   - Some external controllers may show up as `Wireless Controller`
   - For example: `SDL/0/Nintendo Switch Controller` or `SDL/0/Dualsense Wireless Controller`
9. Select the `Motion Input` tab
10. Hover over any of the buttons under the `Accelerometer` or `Gyroscope` sections and press `L2`
11. Select `SDL/0/yourexternalcontrollername` in the drop-down menu at the top
    - For example: `SDL/0/Nintendo Switch Controller`
    - For some controllers, it may be under `SDL/0/Wireless Controller Motion Sensors`
12. Scroll down to the bottom of the list until you see `Accel` and `Gyro` direction inputs
13. Select the matching input to the button you clicked in Step 10
    - ![How to Configure Gyro With External Controllers](../../assets/dolphin-external-controller-gyro.png)
14. Press `Clear` in the bottom right
15. Press `Select` in the top right
16. Press `OK` in the bottom right
17. Repeat for each button under the `Accelerometer` and `Gyroscope` sections
18. (Optional) To use the controller gyro as a pointer (moving the controller itself), check `Enable` under the Pointer section on the left on the `Motion Input` tab
    - Make sure to click `Recenter` and tinker with the settings here to calibrate the pointer
    - You may also want to consider disabling `Auto-hide` under the `Point` section on the `Motion simulation tab`
19. After you are finished, give your profile a name in the top right and save it as a new profile
20. To select this profile, open the controller menu, select the profile name in the drop-down menu and click `Load`

**Note:** Different games have different preferences for Nunchuk and Motionplus support. Under the `General and Options` tab, you may uncheck `Attach MotionPlus` or select the appropriate extension in the drop-down menu. Be sure to create and save a new profile for each circumstance to quickly load the different profiles as needed.

#### Game Mode

1. In Game Mode, connect your controller
2. Select your Wii game
3. On the `Play` screen, select the `Controller` icon to the right of the screen
   - <img src="https://github.com/dragoonDorise/EmuDeck/assets/108900299/468d63e3-534c-4270-ac61-06e167d6df48" height="300">
4. Select your controller tab at the top
   - <img src="https://github.com/dragoonDorise/EmuDeck/assets/108900299/b51a1405-9cdf-4ba3-bebf-db817f057f63" height="300">
5. Click the `Gear` icon to the right, and click `Disable Steam Input`
   - <img src="https://github.com/dragoonDorise/EmuDeck/assets/108900299/33cbcb8e-a444-4a75-8e4a-ba9451e6e07a" height="300">
   - You may need to restart first for this setting to properly apply
6. Your controller's gyro will now work for this selected game, repeat as needed for your other games

#### Post-Configuration

To restore the default Steam Deck controls:

1. Open Dolphin
2. Open the `Controllers` menu
3. Select `Configure` to the right of `Wii Remote 1`
   - Make sure `Wii Remote 1` is set to `Emulated Wii Remote`
4. Select `SDL/0/Virtual Steam Gamepad 1` under `Devices`
5. Select `Wii_base_nunchuck` under `Profile` and click `Load`
6. Click `Close` and exit out of Dolphin

(Optional) To restore Steam Input:

1. Select your Wii game
2. On the `Play` screen, select the `Controller` icon to the right of the screen
   - <img src="https://github.com/dragoonDorise/EmuDeck/assets/108900299/468d63e3-534c-4270-ac61-06e167d6df48" height="300">
3. Select your controller tab at the top
   - <img src="https://github.com/dragoonDorise/EmuDeck/assets/108900299/b51a1405-9cdf-4ba3-bebf-db817f057f63" height="300">
4. Click the `Gear` icon to the right, and click `Enable Steam Input`
   - You may need to restart first for this setting to properly apply
5. The controls will be reverted to Steam Input and the Steam Deck controls will be restored

---

### How to Optimize Performance (Power Tools)

[Back to the Top](#dolphin-table-of-contents)

Visit [Power Tools](../../emudeck-application/steamos/emudeck-application-101.md#power-tools) to learn how to optimize performance using Power Tools.

---

### How to Optimize Storage (Compression Tool)

[Back to the Top](#dolphin-table-of-contents)

To optimize storage, you can use the `EmuDeck Compressor` within EmuDeck.

The `EmuDeck Compressor` will compress your GameCube and Wii ROMs from ISO to RVZ.

After running the `EmuDeck Compression Tool`, re-run Steam ROM Manager to update your ROM shortcuts to the newly compressed ROM.

**Visual Reference:** <img src="https://user-images.githubusercontent.com/108900299/198798630-9cf85bc5-ff42-45c4-bceb-7fc4ac740c3c.png" height="300">

---

### How to Manage Multiple Discs

[Back to the Top](#dolphin-table-of-contents)

M3U files can be used to manage multiple discs for Dolphin. With the `Change Discs Automatically` option toggled (turned on by default with EmuDeck), Dolphin will automatically switch discs in combination with an M3U file.

[Learn how to create an M3U File](../../file-management/steamos/file-management.md#how-to-create-an-m3u-file)

---

### How to Configure Multiplayer

[Back to the Top](#dolphin-table-of-contents)

EmuDeck configures multiplayer out of the box. You do not need to configure the controls. However, to properly set up multiplayer, you will need to enable the additional ports.

**Tutorial**

1. Open the Dolphin emulator
2. Open the `Controller` settings
3. For each controller you are using, including Player 1:
   - GameCube: To the right of each Port # under `GameCube Controllers`, enable `Standard Controller`
     - <img src="https://user-images.githubusercontent.com/108900299/210123946-d7c6a1e8-2cff-420d-b51b-0650327d4525.png" height="300">
   - Wii: To the right of each Port # under `Wii Remotes`, enable `Emulated  Wii Remote`
     - <img src="https://user-images.githubusercontent.com/108900299/210123969-b8bd7928-ef20-4f8f-a5bf-00285f4d2e8f.png" height="300">
4. (Optional) You may need to re-arrange the controller order in Game Mode for your controllers to function as expected. See [How to Re-Arrange the Controller Order](../../controls-and-hotkeys/steamos/external-controllers.md#how-to-re-arrange-the-controller-order) to learn how

**Keep in Mind**

- The Steam Deck profile is automatically set to Port 1
  - For example, if you are using a Steam Deck and two external controllers, you will need to have a total of three ports enabled. However, the first port is enabled by default so you will need to enable two additional ports
- If you are using an external controller as Port 1, you do not need to re-configure any settings in Dolphin. However, you may need to re-arrange the controller order in Game Mode. See [How to Re-Arrange the Controller Order](../../controls-and-hotkeys/steamos/external-controllers.md#how-to-re-arrange-the-controller-order) to learn how
- If you are facing difficulty with matching controllers to their expected ports in Game Mode, you may need to re-arrange the controller order. See [How to Re-Arrange the Controller Order](../../controls-and-hotkeys/steamos/external-controllers.md#how-to-re-arrange-the-controller-order) to learn how
- If you are playing Wii games with GameCube controller support, and would like to use the GameCube controllers, you may need to disable the Wii profiles. See [How to Configure Wii Games To Use A GameCube Controller](#multiplayer) to learn how

---

### How to Configure Multiplayer Controls

[Back to the Top](#dolphin-table-of-contents)

**IMPORTANT:** Multiplayer controllers are fully configured by EmuDeck. If you simply would like to set up multiplayer, see [How to Configure Multiplayer](#how-to-configure-multiplayer). You **do not** need this section if you are satisfied with the default control layout. This section covers how to reconfigure the controls for Players 2-4 if you would rather use a custom configuration.

#### How to Create Multiplayer Profiles

1. In Game Mode, connect your controller(s)
2. In Game Mode, open the Dolphin emulator
   - You may need to add the Dolphin emulator to Steam first using the `Emulators` parser in Steam ROM Manager
3. Click `Options` at the top, click `Controller Settings`
4. Select a system:
   1. For GameCube: Click `Configure` to the right of `Port 1/2/3/4 Standard Controller`
   2. For Wii: Click `Configure` to the right of `Wii Remote 1/2/3/4 Emulated Wii Remote`
5. On this screen, configure your controllers however you like
6. Saving settings:
   - If you would like to save these settings globally, make sure the profile dropdown is blank, and press the `Save` button in the top right
     - Do note that when you update EmuDeck, any global changes **will be reset** to EmuDeck defaults
   - If you would like to save these settings for a specific game, in the top right under `Profile`, enter the profile name you would like to use, and click `Save` to the right

#### How to Use Your Newly Created Controller Profile

If you chose to save your settings globally and you have enabled your multiplayer ports as described in [How to Configure Multiplayer](#how-to-configure-multiplayer), multiplayer should now work with your custom controls.

If you would rather save these settings for a specific game:

**Here's How**

#### How to Apply Multiplayer Profiles On A Per Game Basis

1.  In Desktop Mode, Open the Dolphin emulator
2.  Right click the game you would like to use this controller profile for, and click `Properties`
3.  On the `Game Config` tab, press the `Editor` sub-tab
4.  Under `User Config`, enter a controller profile using the following template:

    - For `SelectedProfileName`, only type the name of the profile, not the file path to the profile
    - Replace the `2` at the end of `WiiMoteProfile2` with the number you would like to apply the profile to. If all the profiles are using the same controller layout, you may simply copy and paste, and only replace the `2` with a `3` and so on.

      **Wii:**

            [Controls]
            WiimoteProfile1 = SelectedProfileName
            WiimoteProfile2 = SelectedProfileName
            WiimoteProfile3 = SelectedProfileName
            WiimoteProfile4 = SelectedProfileName

      **GameCube:**

            [Controls]
            PadProfile1 = SelectedProfileName
            PadProfile2 = SelectedProfileName
            PadProfile3 = SelectedProfileName
            PadProfile4 = SelectedProfileName

5.  Exit out, and your game should now be using the selected profile(s)

For additional information, see [Dolphin's "GameINI (Controller Settings)" Wiki Page](<https://wiki.dolphin-emu.org/index.php?title=GameINI_(Controller_Settings)>).

---

### How to Roll Back Dolphin to an Older Version

[Back to the Top](#dolphin-table-of-contents)

If you do not have access to a mouse and keyboard for the below section, use `L2` to right click and `R2` to left click. Alternatively, remote into your Steam Deck using one of the methods found in the FAQ, [How do I remotely control my Steam Deck?](../../frequently-asked-questions/steamos/index.md#how-do-i-remotely-control-my-steam-deck).

1. In Desktop Mode, open `Konsole`
2. To see a list of prior versions of the emulator, type:
   - `flatpak remote-info --log flathub org.DolphinEmu.dolphin-emu`
3. If Konsole prompts you to select `system` or `user`, enter `2` to select `user`
4. Konsole will list a list of previous versions for the flatpak. The important line for each version is the `Commit: ` line. The `Commit: ` line will have a long accompanying alphanumeric string (the “commit” code). Copy the string for the version you want to downgrade to.
   - Using Citra as an example:
     - ![How to Roll Back Flatpaks: 1](../../assets/how-to-roll-back-flatpaks-1.png)
5. To downgrade to the version you want:
   - `flatpak update --commit=put_commit_code_here org.DolphinEmu.dolphin-emu`
   - Replace `put_commit_code_here` with the actual code you located in Step 2.
     - Using Citra as an example:
       - ![How to Roll Back Flatpaks: 2](../../assets/how-to-roll-back-flatpaks-2.png)

If the above steps did not work and you are getting an error message along the lines of `Flatpak not installed`, your Flatpak is likely installed at the system level instead. Select one of the below solutions:

Solution 1: Open the EmuDeck application, click the `Manage Emulators` page, select the emulator in question, and click `Reinstall / Update`.

Solution 2: Add `sudo` in front of the commands written in Step 2 and Step 5. In Step 2, write `sudo flatpak remote-info --log flathub org.DolphinEmu.dolphin-emu` and in Step 5, write `sudo flatpak update --commit=put_commit_code_here org.DolphinEmu.dolphin-emu`.

---

### How to Configure Language Settings

[Back to the Top](#dolphin-table-of-contents)

#### UI

1. In Desktop Mode, open Dolphin
2. At the top, click `Options`, click `Configuration`
3. Click the `Interface` tab
4. Under `User Interface`, select your preferred language in the drop-down menu

#### In-Game

##### Gamecube

1.  In Desktop Mode, open Dolphin
2.  Right click the game you would like to set the language for
3.  Click `Properties`
4.  Click the `Game Config` tab
5.  Click the `Editor` tab
6.  In the box, type the following:

        [Core]
        GameCubeLanguage = 0

7.  Replace the `0` with the language you would like to use:
    - 0 = English/Japanese
    - 1 = German
    - 2 = French
    - 3 = Spanish
    - 4 = Italian
    - 5 = Dutch

##### Wii

1.  In Desktop Mode, open Dolphin
2.  Right click the game you would like to set the language for
3.  Click `Properties`
4.  Click the `Game Config` tab
5.  Click the `Editor` tab
6.  In the box, type the following:

        [Wii]
        Language = 1

7.  Replace the `0` with the language you would like to use:
    - 0 = Japanese
    - 1 = English
    - 2 = German
    - 3 = French
    - 4 = Spanish
    - 5 = Italian
    - 6 = Dutch
    - 7 = Simplified Chinese
    - 8 = Traditional Chinese
    - 9 = Korean

---

### How to Enable HDR

[Back to the Top](#dolphin-table-of-contents)

With the latest Dolphin update, HDR can now be used on Steam Deck OLEDs. Here's how to enable it.

??? warning

    This section uses instructions copied from this link: https://github.com/ValveSoftware/gamescope/issues/1239. The instructions have been converted to a bash script for ease of use (Step 1 in the instructions below). This section is experimental and installing the Gamescope Flatpak may come with unexpected behavior. This section covers how to install a much older version of Gamescope to match the version used on the Steam Deck. If you accidentally install the latest version, you may notice crashing in other applications. There is a chance that even with the older version installed through the instructions below, you may encounter unexpected crashes or glitches. If you run into any of these issues, uninstall the Gamescope Flatpak through the Discover application in Desktop Mode. Alternatively, run `flatpak remove org.freedesktop.Platform.VulkanLayer.gamescope -y` in Konsole or a terminal of your choice.

1. Download attached `.sh` file
   - [flatpak-gamescope-install.sh](../../configuration-files/flatpak-gamescope-install.sh)
   - For the contents of the script, see [https://raw.githubusercontent.com/EmuDeck/emudeck.github.io/main/docs/configuration-files/flatpak-gamescope-install.sh](https://raw.githubusercontent.com/EmuDeck/emudeck.github.io/main/docs/configuration-files/flatpak-gamescope-install.sh)
2. Place in `/home/deck/Downloads` or a folder of your choice
3. Right click `flatpak-gamescope-install.sh`, click `Properties`, click `Permissions`, check `Is Executable`
4. Right click `flatpak-gamescope-install.sh`, click `Run in Konsole`
5. Wait for it to finish installing
6. In Desktop Mode, open the Dolphin emulator
7. Click the `Graphics` button
8. Click the `Enhancements` tab
9. Check `HDR Post-Processing`
10. Click the `Post-Processing Effect` drop-down menu and select `PerceptualHDR` or `AutoHDR` depending on your preference
    - See the [latest Dolphin blog](https://dolphin-emu.org/blog/2024/04/30/dolphin-progress-report-february-march-and-april-2024/#hdr-enhancements-50-19931-add-autohdr-post-process-shader-by-filoppi-and-50-21232-add-hdr-to-metal-perceptual-hdr-by-samb) for more info on the difference between the two
11. HDR will now be enabled

---

### How to Switch Dolphin to the Development Branch

[Back to the Top](#dolphin-table-of-contents)

RetroAchievements was recently added to Dolphin but can only be used in the development branch until it has been tested thoroughly for public release.

If you are interested in using the development branch to test RetroAchievements or any other Dolphin feature before it is officially released, you may do so by following the steps in this section.

??? warning

    Do keep in mind these builds are experimental and may have bugs. If you are using the development build and request support, make sure to
    include that you are using the development build. If you are using the development build and would like to use netplay, the other
    individual must be on the identical development build version. It is highly recommended you use the stable builds instead if you would
    like to use netplay.

#### How to Switch Dolphin to the Development Branch

1. In Desktop Mode, open Konsole or a terminal of your choice
2. Type each bullet point line one at a time and press enter after each line (if the first two commands do nothing or give you an error, you may skip these):
   - `flatpak remote-delete flathub-beta --system`
   - `flatpak remote-delete flathub-beta --user`
   - `flatpak remote-add --if-not-exists flathub-beta https://flathub.org/beta-repo/flathub-beta.flatpakrepo --user`
   - `flatpak install flathub-beta org.DolphinEmu.dolphin-emu --user -y`
3. The development version of Dolphin has now been installed. To switch to the development branch as the primary version of Dolphin, type the following and press enter:
   - `flatpak make-current org.DolphinEmu.dolphin-emu beta --user`

To switch back to the "Stable" build ("Releases" on the Dolphin website), type the following and press enter:

`flatpak make-current org.DolphinEmu.dolphin-emu stable --user`

If you had Dolphin installed at the system level, you will need to type the following instead:

`sudo flatpak make-current org.DolphinEmu.dolphin-emu stable`

!!! tip "Controls"

    If the controls are not working, first add Dolphin to Steam. To add Dolphin to Steam, either right click Dolphin (`L2`) in the "Applications Launcher" in Desktop Mode, click `Add to Steam` **or** add Dolphin to Steam using the "Emulators" parser in Steam ROM Manager.

    In Game Mode, open Dolphin, at the top, click `Options`, click `Controller Settings`. To the right of `Port 1: Standard Controller` under `GameCube Controllers`, click `Configure` and change the `Device` in the top left to `SDL/0/Steam Deck Controller`. Close out of this window (click the `STEAM` button and click the `X` button on the controller).

    Click `Configure` to the right of `Emulatd Wii Remote` under `Wii Remotes`. Change the `Device` in the top left to `SDL/0/Steam Deck Controller`. Close out of this window (click the `STEAM` button and click the `X` button on the controller).

    At the top, click `Options`, `Hotkey Settings`. Change the `Device` in the top left to `SDL/0/Steam Deck Controller`. Close out of this window (click the `STEAM` button and click the `X` button on the controller).

    Exit Dolphin and the controls will work again in game.

---
