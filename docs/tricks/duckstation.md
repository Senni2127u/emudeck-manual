# <img src="/assets/emulators/duckstation.png" alt="EmuDeck guide" width="80" style="vertical-align: middle"> DuckStation Tips and Tricks

[TOC]

---

### How to Optimize Storage (Compression Tool)

[Back to the Top](#duckstation-table-of-contents)

To optimize storage, you can use the `EmuDeck Compressor` within EmuDeck.

The `EmuDeck Compressor` will compress your Playstation 1 ROMs from ISO or BIN/CUE to CHD. If your ROM is a BIN/CUE, the Compression Tool will only compress it if you have both the BIN and the CUE files for a ROM. If the ROM is in a zip file or is missing a paired BIN or CUE file, the Compression Tool will not detect the ROM.

After running the `EmuDeck Compression Tool`, re-run Steam ROM Manager to update your ROM shortcuts to the newly compressed ROM.

**Visual Reference:** <img src="https://user-images.githubusercontent.com/108900299/198798630-9cf85bc5-ff42-45c4-bceb-7fc4ac740c3c.png" height="300">

---

### How to Manage Multiple Discs

[Back to the Top](#duckstation-table-of-contents)

M3U files can be used to manage multiple discs for DuckStation. When the time comes to switch discs, use the Left Trackpad Touch Menu Hotkey. A full list of hotkeys and a tutorial on how to use Steam Input profiles can be found here: #hotkeys.

[Learn how to create an M3U File](../../file-management/steamos/file-management.md#how-to-create-an-m3u-file)

---

### How to Use Cheats

[Back to the Top](#duckstation-table-of-contents)

1. While in game, either: press `Start` and `R2` or use the left Trackpad and select the `Quick Menu` icon
   - Steam Input profiles for PlayStation 1 ROMs and ES-DE are enabled by default. However, if you do not see the Trackpad menu, see [How to Select a Steam Input Profile](../../controls-and-hotkeys/steamos/hotkeys.md#how-to-select-a-steam-input-profile)
2. Click `Cheat List`
3. Select which cheats you would like to use

---

### How to Configure Multiplayer

[Back to the Top](#duckstation-table-of-contents)

Multiplayer for DuckStation is configured out of the box, no additional configuration is needed.

You may need to re-arrange the controller order in Game Mode for your controllers to function as expected. See [How to Re-Arrange the Controller Order](../../controls-and-hotkeys/steamos/external-controllers.md#how-to-re-arrange-the-controller-order) for more information.

---

### How to Roll Back DuckStation to an Older Version

[Back to the Top](#duckstation-table-of-contents)

If you do not have access to a keyboard for the below section, use `L2` to right click and `R2` to left click. Alternatively, remote into your Steam Deck using one of the methods found in the FAQ, [How do I remotely control my Steam Deck?](../../frequently-asked-questions/steamos/index.md#how-do-i-remotely-control-my-steam-deck).

1. In Desktop Mode, open `Konsole`
2. To see a list of prior versions of the emulator, type:
   - `flatpak remote-info --log flathub org.duckstation.DuckStation`
3. If Konsole prompts you to select `system` or `user`, enter `2` to select `user`
4. Konsole will list a list of previous versions for the flatpak. The important line for each version is the `Commit: ` line. The `Commit: ` line will have a long accompanying alphanumeric string (the “commit” code). Copy the string for the version you want to downgrade to.
   - Using Citra as an example:
     - ![How to Roll Back Flatpaks: 1](../../assets/how-to-roll-back-flatpaks-1.png)
5. To downgrade to the version you want:
   - `flatpak update --commit=put_commit code_here org.duckstation.DuckStation`
   - Replace `put_commit code_here` with the actual code you located in Step 2.
     - Using Citra as an example:
       - ![How to Roll Back Flatpaks: 2](../../assets/how-to-roll-back-flatpaks-2.png)

If the above steps did not work and you are getting an error message along the lines of `Flatpak not installed`, your Flatpak is likely installed at the system level instead. Select one of the below solutions:

Solution 1: Open the EmuDeck application, click the `Manage Emulators` page, select the emulator in question, and click `Reinstall / Update`.

Solution 2: Add `sudo` in front of the commands written in Step 2 and Step 5. In Step 2, write `sudo flatpak remote-info --log flathub org.duckstation.DuckStation` and in Step 5, write `sudo flatpak update --commit=put_commit_code_here org.duckstation.DuckStation`.

---

### How to Configure Language Settings

[Back to the Top](#duckstation-table-of-contents)

#### UI

1. In Desktop Mode, open DuckStation
2. At the top, click `Settings`
3. Click `Language`
4. Select your preferred language in the drop-down menu

#### In-Game

Some games may not have language options. For a full list of which games have language options, click one of the below links.

- PAL: [https://psxdatacenter.com/pal_list.html](https://psxdatacenter.com/pal_list.html)
- United States: [https://psxdatacenter.com/ntsc-u_list.html](https://psxdatacenter.com/ntsc-u_list.html)
- Japan: [https://psxdatacenter.com/ntsc-j_list.html](https://psxdatacenter.com/ntsc-j_list.html)

1. Launch a game that supports your preferred language
2. Depending on the game:
   - Select your preferred language on the initial launch of the game
   - In the main menu of the game, open the Options menu and select your preferred language

---
