# <img src="/assets/emulators/flycast.png" alt="EmuDeck guide" width="80" style="vertical-align: middle"> Flycast Tips and Tricks

[TOC]

---

### HLE BIOS



HLE BIOS is **enabled by default** for Dreamcast games. BIOS for Dreamcast games is **optional**. However, some games may not perform as expected with the HLE BIOS or you may need additional features provided by console dumped BIOS.

In order to use console dumped BIOS, you may place the files required into the `Emulation/bios/flycast/bios` folder. You will also need to disable HLE BIOS in the Flycast GUI.

![Flycast HLE BIOS](../../assets/flycast-hle-bios.png)

---

### How to Install Custom Textures



**Texture Pack Sources**

_This list is not exhaustive_

- [https://old.reddit.com/r/Flycast_texture_packs/](https://old.reddit.com/r/Flycast_texture_packs/)

1. Open the `/home/deck/.var/app/org.flycast.Flycast/data/` folder
   - `~/.var` is a hidden folder by default. In Dolphin (file manager), click the hamburger menu in the top right, click `Show Hidden Files` to see these folders
2. Create two folders: `TEXDUMP` and `TEXTURES`, casing matters
3. Place your texture pack(s) in `/home/deck/.var/app/org.flycast.Flycast/data/TEXTURES`
4. Open Flycast, click the `Video` tab, scroll to the `Texture Upscaling` section, check `Load Custom Textures`
5. Your texture pack will now be installed

---

### How to Configure the Sega Dreamcast Microphone



For a full list of games that used the Sega Dreamcast Microphone, see [https://segaretro.org/Dreamcast_Microphone](https://segaretro.org/Dreamcast_Microphone).

1. Open Flycast
2. Click the `Controls` tab
3. Under the `Dreamcast Devices` section, on the `Port A` controller, set the first port to `Sega VMU` and the second port to `Microphone`
4. Exit out of Flycast and your microphone will now automatically be enabled

To set this on a per-game setting:

1. Open the respective game
2. Press the `Select` button
3. Click `Settings`
4. Click the `Controls` tab
5. Under the `Dreamcast Devices` section, on the `Port A` controller, set the first port to `Sega VMU` and the second port to `Microphone`
6. Click `Make Game Config` at the top of the screen
7. Exit out of the settings and your microphone will only be enabled for this game

---

### How to Configure Light Gun Games



#### Flycast Controls

1. Open a game with light gun support
2. Press `STEAM` or `...` + `DPad Down` to open the `Quick Menu`
3. At the top, click `Make Game Config`
4. Click the `Controls` Tab
5. Scroll down to `Dreamcast Devices`
6. Set the `Port A` controller to `Light Gun` and check the `Crosshair` box

#### Steam Input

1. In Game Mode, single click the game you would like to change the Steam Input Profile for, and click the `Controller Icon` on the right of the screen. Click the layout (whichever name it is currently set to) at the top
2. Click the `Templates` tab
3. Select the `EmuDeck - Steam Deck Light Gun Controls` profile
4. Light gun controls will now be configured for this game

{{ read_csv('emudeck-steam-deck-light-gun-controls.csv') }}

---
