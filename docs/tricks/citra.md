# <img src="/assets/emulators/citra.png" alt="EmuDeck guide" width="80" style="vertical-align: middle"> Citra Tips and Tricks

[TOC]

---

### How to Configure Gyro



Gyro for Citra requires SteamDeckGyroDSU. SteamDeckGyroDSU can be installed via EmuDeck, or it can be installed manually.

Visit [SteamDeckGyroDSU](../../emudeck-application/steamos/emudeck-application-101.md#steamdeckgyrodsu) to learn how to install and utilize SteamDeckGyroDSU.

---

### How to Configure Gyro With External Controllers



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
   <img src="https://github.com/dragoonDorise/EmuDeck/assets/108900299/24945d4c-df06-4fbe-9668-7becea0c5edb" height="300">
4. Open Citra
5. Click `Emulation` at the top, click `Configure`
6. Click `Controls` on the left
7. Click `New` to the right of `Profile` and give it a unique name
8. Click `Motion / Touch..` in the bottom left
9. To the right of `Motion Provider`, select `SDL` in the drop-down menu
10. Click `Configure` and follow the instructions
11. Click `OK`
12. Click `OK` again and exit out of Citra
13. Switch to `Game Mode`

#### Game Mode

1. In Game Mode, connect your controller
2. Select your Nintendo 3DS game
3. On the `Play` screen, select the `Controller` icon to the right of the screen
   <img src="https://github.com/dragoonDorise/EmuDeck/assets/108900299/468d63e3-534c-4270-ac61-06e167d6df48" height="300">
4. Select your controller tab at the top
   <img src="https://github.com/dragoonDorise/EmuDeck/assets/108900299/b51a1405-9cdf-4ba3-bebf-db817f057f63" height="300">
5. Click the `Gear` icon to the right, and click `Disable Steam Input`
   <img src="https://github.com/dragoonDorise/EmuDeck/assets/108900299/33cbcb8e-a444-4a75-8e4a-ba9451e6e07a" height="300">
   - You may need to restart first for this setting to properly apply
6. Your controller's gyro will now work for this selected game, repeat as needed for your other games

#### Post-Configuration

To restore the default Steam Deck controls:

1. Open Citra
2. Click `Emulation` at the top, click `Configure`
3. Click `Controls` on the left
4. To the right of `Profile`, select `SD-Default` in the drop-down menu
5. Click `OK` and exit out of Citra

(Optional) To restore Steam Input:

1. Select your Nintendo 3DS game
2. On the `Play` screen, select the `Controller` icon to the right of the screen
   <img src="https://github.com/dragoonDorise/EmuDeck/assets/108900299/468d63e3-534c-4270-ac61-06e167d6df48" height="300">
3. Select your controller tab at the top
   <img src="https://github.com/dragoonDorise/EmuDeck/assets/108900299/b51a1405-9cdf-4ba3-bebf-db817f057f63" height="300">
4. Click the `Gear` icon to the right, and click `Enable Steam Input`
   - You may need to restart first for this setting to properly apply
5. The controls will be reverted to Steam Input and the Steam Deck controls will be restored

---

### How to Optimize Performance (Power Tools)



Visit [Power Tools](../../emudeck-application/steamos/emudeck-application-101.md#power-tools) to learn how to optimize performance using Power Tools.

---

### How to Install Custom Textures



Here's how to install custom textures for Citra:

#### Citra Configuration

1. In Desktop Mode, open Citra
2. Click `Emulation` in the top left. Click `Configuration`, `Graphics`, and check both `Use Custom Textures` and `Async Custom Texture Loading`
   <img src="https://user-images.githubusercontent.com/108900299/236593948-5a918187-27a7-4f5f-ac64-3b3147be8825.png" height="300">

**Note:** `Preload Custom Textures` is no longer recommended. Leave `Preload Custom Textures` off

#### How to Install Custom Textures

**Note:** Your texture pack may already come properly named and packaged with the correct `TitleID` and texture files. You may place the included texture pack folder directly into `/home/deck/.local/share/citra-emu/textures/`. You do not need the following section if this is the case.

1. In Desktop Mode, open [https://3ds.jdbye.com/?details=USA&split=0&display=0](https://3ds.jdbye.com/?details=USA&split=0&display=0) in a browser
2. Note down the `Title ID` for the game
   - For example, The Legend of Zelda: Majora's Mask 3D's (US) Title ID is: `0004000000125500`
3. Open `/home/deck/.local/share/citra-emu/textures/`
   - `~/.local` is a hidden folder by default. In Dolphin (file manager), click the hamburger menu in the top right, click `Show Hidden Files` to see these folders
4. In the `textures` folder from Step 3, create a folder matching the `TitleID` from Step 2
5. Put your texture files directly into the `TitleID` folder you created in Step 4
6. Your texture pack should now be installed

!!! tip

    Consider enabling `Preload Custom Textures`. This may help performance in some cases.

---

### How to Use Cheats



**Cheat Sources**

_This list is not exhaustive_

- [https://github.com/iSharingan/CTRPF-AR-CHEAT-CODES/tree/master/Cheats](https://github.com/iSharingan/CTRPF-AR-CHEAT-CODES/tree/master/Cheats)

#### How to Use Cheats

1. In Desktop Mode, open Citra
2. Right click a game of your choice, click `Properties`
   <img src="https://user-images.githubusercontent.com/108900299/236593492-91df7ce3-efae-4bb7-a559-7c252637a2e4.png" height="300">
3. Click the `Cheats` tab
   <img src="https://user-images.githubusercontent.com/108900299/236593531-c045ab6e-3779-4c5a-b6ce-0af4a243f121.png" height="300">
4. Click `Add Cheat`
5. Name the cheat and add the code to the box under `Code:`
   <img src="https://user-images.githubusercontent.com/108900299/236593755-85163908-cc80-4684-a343-01f180f14365.png" height="300">
6. Click Save in the top right
7. Check the box to the left of the cheat to enable it
   <img src="https://user-images.githubusercontent.com/108900299/236593806-1f8973a4-cd67-4c35-b18e-14a5fbb30105.png" height="300">

---

### How to Roll Back Citra to an Older Version



If you do not have access to a mouse and keyboard for the below section, use `L2` to right click and `R2` to left click. Alternatively, remote into your Steam Deck using one of the methods found in the FAQ, [How do I remotely control my Steam Deck?](../../frequently-asked-questions/steamos/index.md#how-do-i-remotely-control-my-steam-deck).

1. In Desktop Mode, open `Konsole`
2. To see a list of prior versions of the emulator, type:
   - `flatpak remote-info --log flathub org.citra_emu.citra`
3. If Konsole prompts you to select `system` or `user`, enter `2` to select `user`
4. Konsole will list a list of previous versions for the flatpak. The important line for each version is the `Commit: ` line. The `Commit: ` line will have a long accompanying alphanumeric string (the “commit” code). Copy the string for the version you want to downgrade to.
   - ![How to Roll Back Flatpaks: 1](../../assets/how-to-roll-back-flatpaks-1.png)
5. To downgrade to the version you want:
   - `flatpak update --commit=put_commit_code_here org.citra_emu.citra`
   - Replace `put_commit_code_here` with the actual code you located in Step 2.
     - For example:
       - ![How to Roll Back Flatpaks: 2](../../assets/how-to-roll-back-flatpaks-2.png)

If the above steps did not work and you are getting an error message along the lines of `Flatpak not installed`, your Flatpak is likely installed at the system level instead. Select one of the below solutions:

Solution 1: Open the EmuDeck application, click the `Manage Emulators` page, select the emulator in question, and click `Reinstall / Update`.

Solution 2: Add `sudo` in front of the commands written in Step 2 and Step 5. In Step 2, write `sudo flatpak remote-info --log flathub org.citra_emu.citra` and in Step 5, write `sudo flatpak update --commit=put_commit_code_here org.citra_emu.citra`.

---

### How to Configure Language Settings



#### UI

1. In Desktop Mode, open Citra
2. At the top, click `Emulation`, click `Configure`
3. On the left hand-side of the screen, click `General`
4. Click the `UI` tab
5. Under `General`, select your preferred language in the drop-down menu

#### In-Game

1. In Desktop Mode, open Citra
2. At the top, click `Emulation`, click `Configure`
3. On the left hand-side of the screen, click `System`
4. Click the `System` tab
5. Under `System Settings`, select your preferred language in the drop-down menu

---
