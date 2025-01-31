# <img src="/assets/emulators/primehack.png" alt="EmuDeck guide" width="80" style="vertical-align: middle"> PrimeHack Tips and Tricks

[TOC]

---

### How to Optimize Performance (Power Tools)



Visit [Power Tools](../../emudeck-application/steamos/emudeck-application-101.md#power-tools) to learn how to optimize performance using Power Tools.

---

### How to Optimize Storage (Compression Tool)



To optimize storage, you can use the `EmuDeck Compression Tool` in the `Tools & Stuff` menu within EmuDeck.

The `EmuDeck Compression Tool` will compress your Metroid Prime Trilogy ROM from ISO to RVZ.

After running the `EmuDeck Compression Tool`, re-run Steam ROM Manager to update your ROM shortcuts to the newly compressed ROM.

**Visual Reference:** <img src="https://user-images.githubusercontent.com/108900299/198798630-9cf85bc5-ff42-45c4-bceb-7fc4ac740c3c.png" height="300">

---

### How to Install Custom Textures



Here's how to install custom textures for PrimeHack:

1. Open the PrimeHack emulator, click `Graphics` in the top right (or `Options` > `Graphic Settings`), click `Advanced`, make sure `Load Custom Textures` and `Prefetch Custom Textures` are checked.
   <img src="https://user-images.githubusercontent.com/108900299/196001972-9b887344-b246-4c3d-9109-dfc9d76840f3.png" height="200">
2. Open `/home/deck/.var/app/io.github.shiiion.primehack/data/dolphin-emu/Load/Textures`
   - `~/.var` is an invisible folder by default. In Dolphin (file manager), click the hamburger menu in the top right, click `Show Hidden Files` to see these folders.
   - If the `Load` and `Textures` folder do not exist, create them.
   - Visual Reference: <img src="https://user-images.githubusercontent.com/108900299/196001948-ae428327-5ca5-4a1a-b649-2a620678790c.png" height="200">
3. In the `Textures` folder from Step 2, create a folder named `R3M`.
4. Put your texture files directly into this folder.
5. Your texture pack should now be installed.
   - If the game crashes with custom textures, it is likely too demanding for the Steam Deck. You can turn off `Prefetch Custom Textures` as a workaround, but performance will still take a hit.

---

### How to Configure PrimeHack to work with ES-DE



You need to move your `Metroid Prime Trilogy` ROM to `Emulation/roms/wii` and choose an alternative emulator for the ROM in ES-DE.

For further instructions, refer to: [How to Select a Different Emulator on a Per Game Basis](../../tools/steamos/es-de.md#how-to-select-a-different-emulator-on-a-per-game-basis).

---

### How to Roll Back PrimeHack to an Older Version



If you do not have access to a mouse and keyboard for the below section, use `L2` to right click and `R2` to left click. Alternatively, remote into your Steam Deck using one of the methods found in the FAQ, [How do I remotely control my Steam Deck?](../../frequently-asked-questions/steamos/index.md#how-do-i-remotely-control-my-steam-deck).

1. In Desktop Mode, open `Konsole`
2. To see a list of prior versions of the emulator, type:
   - `flatpak remote-info --log flathub io.github.shiiion.primehack`
3. If Konsole prompts you to select `system` or `user`, enter `2` to select `user`
4. Konsole will list a list of previous versions for the flatpak. The important line for each version is the `Commit: ` line. The `Commit: ` line will have a long accompanying alphanumeric string (the “commit” code). Copy the string for the version you want to downgrade to.
   - Using Citra as an example:
     - ![How to Roll Back Flatpaks: 1](../../assets/how-to-roll-back-flatpaks-1.png)
5. To downgrade to the version you want:
   - `flatpak update --commit=put_commit_code_here io.github.shiiion.primehack`
   - Replace `put_commit_code_here` with the actual code you located in Step 2.
     - Using Citra as an example:
       - ![How to Roll Back Flatpaks: 2](../../assets/how-to-roll-back-flatpaks-2.png)

If the above steps did not work and you are getting an error message along the lines of `Flatpak not installed`, your Flatpak is likely installed at the system level instead. Select one of the below solutions:

Solution 1: Open the EmuDeck application, click the `Manage Emulators` page, select the emulator in question, and click `Reinstall / Update`.

Solution 2: Add `sudo` in front of the commands written in Step 2 and Step 5. In Step 2, write `sudo flatpak remote-info --log flathub io.github.shiiion.primehack` and in Step 5, write `sudo flatpak update --commit=put_commit_code_here io.github.shiiion.primehack`.

---

### How to Configure Language Settings



#### UI

1. In Desktop Mode, open PrimeHack
2. At the top, click `Options`, click `Configuration`
3. Click the `Interface` tab
4. Under `User Interface`, select your preferred language in the drop-down menu

#### In-Game

1.  In Desktop Mode, open PrimeHack
2.  Right click "Metroid Prime: Trilogy"
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
