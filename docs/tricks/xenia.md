# <img src="/assets/emulators/xenia.png" alt="EmuDeck guide" width="80" style="vertical-align: middle"> Xenia Tips and Tricks

[TOC]

---

### Troubleshooting Tips

[Back to the Top](#xenia-table-of-contents)

- As a first step, Reset Xenia on the Manage Emulators page in the EmuDeck application
- If you get a Wine related error, make sure your ROMs are in `Emulation/roms/xbox360/roms` or `Emulation/roms/xbox360/roms/xbla`, **not** `Emulation/roms/xbox360`
- If you are getting a `!Status or GPU Command Error Messages`, read [How to Fix !Status or GPU Command Error Messages](#how-to-fix-status-or-gpu-command-error-messages)
- If you are still on an older version of Xenia, try updating to the latest version and use DX12 instead of Vulkan, see [How to Swap Between Vulkan and DX12](#how-to-swap-between-vulkan-and-dx12)
- If Xenia was working perfectly fine and suddenly stopped working, see [How to Delete Xenia's Prefix](#how-to-delete-xenias-prefix)
- If you are noticing game specific issues, search for your game on Xenia's game compatibility database, [https://github.com/xenia-project/game-compatibility/issues](https://github.com/xenia-project/game-compatibility/issues) and see if users have suggested any solutions
  - If you need to make any edits to the configuration file, open `xenia-canary.config.toml` in `Emulation/roms/xbox360`
- If you are playing Xbox Live Arcade Games, make sure to read [How to Set Up Xbox Live Arcade Games](#how-to-set-up-xbox-live-arcade-games)

---

### How to Configure Multiplayer

[Back to the Top](#xenia-table-of-contents)

Multiplayer for Xenia is configured out of the box, no additional configuration is needed.

You may need to re-arrange the controller order in Game Mode for your controllers to function as expected. See [How to Re-Arrange the Controller Order](../../controls-and-hotkeys/steamos/external-controllers.md#how-to-re-arrange-the-controller-order) for more information.

---

### How to Swap Out Xenia Builds

[Back to the Top](#xenia-table-of-contents)

Xenia, through Proton/Wine, is currently in an experimental state. Updates may break or affect the emulator in unexpected ways. If an update does break certain games launching from Xenia, it is easy to swap out the build for an older one so you can continue playing.

This section will go over how to swap out the latest build of Xenia Canary for `e9d1e51_canary_experimental` as an example. However, you can take what is written here and apply it to any build of Xenia Canary as well.

**Tutorial**

1. In Desktop Mode, download `xenia_canary.zip` from: [https://github.com/xenia-canary/xenia-canary/releases/tag/e9d1e51](https://github.com/xenia-canary/xenia-canary/releases/tag/e9d1e51)
2. Extract the zip file to a folder of your choice
3. Copy or move `xenia_canary.exe` in the newly extracted folder to `Emulation/roms/xbox360` and overwrite the pre-existing `xenia_canary.exe`
4. To test, you can open Xenia by launching `xenia.sh` from `Emulation/tools/launchers` or `xenia (Proton)` from the applications launcher in the bottom left
5. Xenia will now be using your swapped out build. However, you can update to the latest build at any time through EmuDeck

**Visual Tutorial**

<figure class="video_container">
  <video controls="true" allowfullscreen="true">
    <source src="/videos/how-to-swap-out-xenia-builds.mp4" type="video/mp4">
  </video>
</figure>

---

### How to Swap Between Vulkan and DX12

[Back to the Top](#xenia-table-of-contents)

Recent (as of August 2023) updates of Proton Experimental increased compatibility for DX12. These updates allow more games to boot through Xenia using DX12. At the moment, EmuDeck sets Xenia to Vulkan by default, but swapping between the two is fairly easy.

**Here's How**

1. Open `Emulation/roms/xbox360`
2. Right click `xenia-canary.config.toml` and click `Open with Kate` or a text editor of your choice
3. Locate the `gpu = ""` line
   - By default through EmuDeck, this line should write `gpu = "vulkan"`
4. To swap between Vulkan and DX12, select one of the two below and write it on the `gpu=""` line:
   - Vulkan:
     - `gpu = "vulkan"`
   - DX12:
     - `gpu ="d3d12"`
   - `"vulkan"` and `"d3d12"` must be in quotes

**Photos**

Vulkan:

![How to Swap Between Vulkan and DX12: Vulkan](../../assets/how-to-swap-between-vulkan-and-dx12-1.png)

DX12:

![How to Swap Between Vulkan and DX12: DX12](../../assets/how-to-swap-between-vulkan-and-dx12-2.png)

**Video**

<figure class="video_container">
  <video controls="true" allowfullscreen="true">
    <source src="/videos/how-to-swap-between-vulkan-and-dx12.mp4" type="video/mp4">
  </video>
</figure>

---

### How to Manage Multiple Discs

[Back to the Top](#xenia-table-of-contents)

Xenia does not support M3U files.

Xbox 360 Multi-disc games are not all the same. Some Xbox 360 multi-disc games may contain the disc content on Disc 1 and optional content on Disc 2, allowing you to complete the entire game using only Disc 1. Some Xbox 360 multi-disc games are split in parts, requiring you to use all included discs to complete the game. Some may contain the entire game on Disc 1 and allow you to install additional content from the other discs, similar to DLC.

#### Xbox 360 Games With Optional Content on Separate Discs

You can treat each disc as separate "games", and only need Disc 1 to complete the full base game.

**List of Games**

- Red Dead Redemption
  - The entire base game is on Disc 1 and the Undead Nightmare DLC and multiplayer are on Disc 2

#### Xbox 360 Games With Split Parts on Each Disc

Xenia Canary will prompt you to select the next disc after you complete one disc. If you are using Steam ROM Manager, you may elect to only parse Disc 1 and hide any additional discs, see [How to Manage ROMs with Multiple Discs](../../tools/steamos/steam-rom-manager.md#how-to-manage-roms-with-multiple-discs) to learn how.

**List of Games**

- Lost Odyssey
  - Each disc contains a portion of the full content

#### Xbox 360 Games With Installable Content on Additional Discs

To download the content on the additional discs and use it on the base disc , you will need to install them and treat them as "DLC". Xenia does not have a way of directly supporting this yet. There may be other ways to accomplish installing the additional content, but this wiki will not cover those methods.

**List of Games**

- Call of Duty: Advanced Warfare

---

### How to Set Up Xbox Live Arcade Games

[Back to the Top](#xenia-table-of-contents)

#### File Format

Xbox Live Arcade ROMs typically come in nested folders with an alphanumerically named file.

For example, Banjo Kazooie:

```
Banjo Kazooie
└── 58410954
    └── 000D0000
        └── DA78E477AA5E31A7D01AE8F84109FD4BF89E49E8
```

The `DA78E477AA5E31A7D01AE8F84109FD4BF89E49E8` file is the game file used to launch Banjo Kazooie.

To make this format easier to use with both Steam ROM Manager and ES-DE, rename the game file to match the game name. Using Banjo Kazooie as an example, rename `DA78E477AA5E31A7D01AE8F84109FD4BF89E49E8` to `Banjo Kazooie`.

Move the newly renamed `Banjo Kazooie` file to `Emulation/roms/xbox360/roms/xbla`. **Note the second roms folder.**

Use the `Microsoft Xbox 360 - Xenia - XBLA` parser in Steam ROM Manager or ES-DE to play your game. You **do not** need any of the additional folders included with the original ROM. You may delete these folders.

#### Xenia Configuration

In order to play Xbox Live Arcade Games, you also need the full license. Xenia makes activating this license fairly easy.

**Here's How**

1. Open `Emulation/roms/xbox360`
2. Right click `xenia-canary.config.toml` and click `Open with Kate` or a text editor of your choice
3. Locate the `license_mask = ` line
   - By default, this line should write `license_mask = 0`
4. To activate Xbox Live Arcade ROMs, change the `0` to a `1`:
   - `license_mask = 1`

**Photos**

Unactivated License:

![How to Set Up Xbox Live Arcade Games: Unactivated](../../assets/how-to-set-up-xbox-live-arcade-games-unactivated.png)

Activated License:

![How to Set Up Xbox Live Arcade Games: Activated](../../assets/how-to-set-up-xbox-live-arcade-games-activated.png)

---

### How to Delete Xenia's Prefix

[Back to the Top](#xenia-table-of-contents)

Since Xenia is packaged as a Windows application and has no Linux version widely available, EmuDeck downloads and runs Xenia through Proton using a script. All of Xenia's important files (saves and configurations) are localized to Xenia's folder in `Emulation/roms/xbox360`.

However, running Xenia through Proton will still create a prefix (a sort of Windows virtual C:Drive). If you notice Xenia suddenly stops working (after it was previously working), you may try deleting the prefix. Deleting the prefix will not delete any of your saves or configurations since these are localized to the `Emulation/roms/xbox360` folder.

**IMPORTANT:** If you changed Xenia's Proton version in `Emulation/tools/launchers/xenia.sh`, and notice Xenia suddenly stops working, it's recommended to delete the prefix. Deleting the prefix will "flush" Xenia and give it a clean slate (while retaining saves and configurations) with your newly selected Proton version.

#### How to Delete Xenia's Prefix

1. In Desktop Mode, open Xenia
   - [How to Launch Xenia in Desktop Mode](#how-to-launch-xenia-in-desktop-mode)
   - It does not matter if Xenia actually opens on this step. If opening Xenia does not do anything, proceed to Step 2
2. Open the `Emulation/tools` folder
3. Right click `proton-launch.log` and click `Open with Kate` or a text editor of your choice
4. Locate the `PFX: ` line
   - For example: `PFX: /home/deck/.local/share/Steam/steamapps/compatdata/3322499838`
5. Navigate to the path on the `PFX: ` line in Dolphin
6. Delete the numerical folder at the end of the path
   - For example, with `PFX: /home/deck/.local/share/Steam/steamapps/compatdata/3322499838`, delete the folder named `3322499838` in `/home/deck/.local/share/Steam/steamapps/compatdata`
7. Re-open Xenia in Desktop Mode to re-generate the prefix
8. Close out of Xenia and you may continue playing in Game Mode

---

### How to Configure Language Settings

[Back to the Top](#xenia-table-of-contents)

#### In-Game

1. In Desktop Mode, open the `Emulation/roms/xbox360` folder
2. Right click `xenia-canary.config.toml` and click `Open with Kate` or a text editor of your choice
3. Scroll down to the `XConfig` section, locate `user_language = 1`
4. Replace `1` with your preferred language:
   - 1=en
   - 2=ja
   - 3=de
   - 4=fr
   - 5=es
   - 6=it
   - 7=ko
   - 8=zh
   - 9=pt
   - 11=pl
   - 12=ru
   - 13=sv
   - 14=tr
   - 15=nb
   - 16=nl
   - 17=zh
5. Save and exit out of the text file

---

### How to Apply Patches

[Back to the Top](#xenia-table-of-contents)

When you install Xenia through EmuDeck, a collection of game patches are also automatically downloaded to your `Emulation/roms/xbox360/patches` folder. These patches provide ways to fix various issues in games.

**To apply patches:**

1. In Desktop Mode, open the `Emulation/roms/xbox360/patches` folder
2. Right click a text file matching your game name or game ID and click `Open with Kate` or a text editor of your choice
3. Each text file will typically have multiple patches identified with the `[[patch]]` header and the name of the patch below the header. Select a patch to enable and locate the `is_enabled` field
4. On the `is_enabled` field, change `false` to `true`
5. Save the text file and exit out
6. The patch you selected will now be applied for your game

Do note that if your game ID does not match the ID in the patch, the patch may not apply. Game IDs typically vary depending on the region or version of your game. For example, the patches folder contains multiple patch files for "Project Gotham Racing" depending on which version of the game you have. Ensure that your game version matches the patch file you are using and the patch will successfully apply to your game.

---

### How to Set Game Settings On a Per-Game Basis

[Back to the Top](#xenia-table-of-contents)

For a full list of Xenia configurations, see [https://github.com/xenia-canary/xenia-canary/wiki/Options](https://github.com/xenia-canary/xenia-canary/wiki/Options).

Depending on which front-end you are using, the below sections will cover how to apply the Xenia configurations as flags for your games. To convert these configurations into flags, remove any spaces and add two dashes to the beginning of the config name.

A few examples:

**Xenia Config**

`license_mask = #`

`user_language = #`

`gpu = string`

`mount_cache = bool`

**Xenia Flag**

In order to enable license mask:

- `--license_mask=1`

To set Polish as the language:

- `--user_language=11`

To set the GPU as vulkan:

- `--gpu="vulkan"`

To enable mount_cache:

- `--mount_cache=true`

#### ES-DE

1. In Desktop Mode, open the `Emulation/roms/xbox360/roms` folder or `Emulation/roms/xbox360/roms/xbla` folder
2. Right click anywhere in the folder, click `Create New --> Text File`
3. Match the name of the text file to the game and set the file extension to `.esprefix`
   - For example:
     - ROM Name: `Peggle`
     - New text file name: `Peggle.esprefix`
4. Open the newly created text file in Kate or a text editor of your choice
5. On a single line, write:
   - `--configname=configvalue`
     - For example:
       - `--license_mask=1`
       - `--user_language=11`
       - `--gpu="vulkan"`
       - `--mount_cache=true`
6. The config you set will now be applied to this specific game in ES-DE

#### Pegasus

1.  In Desktop Mode, open the `Emulation/roms/xbox360/roms` folder
2.  Right click `metadata.txt`, click `Open with Kate` or a text editor of your choice
3.  At the bottom of the text file, add a new section using the following format:

        game: GAMENAME
        file: FILENAME
        launch: /PATH/TO/xenia.sh "Z:{file.path}" --CONFIGNAME=CONFIGVALUE

4.  Replace GAMENAME with the name of the game
    - For example:
      - `Banjo-Kazooie - Nuts & Bolts`
5.  Replace FILENAME with the file name
    - For example:
      - `Banjo-Kazooie - Nuts & Bolts.iso`
    - If your ROM is in `Emulation/roms/xbox360/roms/xbla`, write `xbla/FILENAME`
      - For example:
        - `xbla/Peggle`
6.  Edit `/PATH/TO` with the path to `xenia.sh`, the path for `xenia.sh` will be at the top of the `metadata.txt` file, you may copy it here
7.  Edit `--CONFIGNAME=CONFIGVALUE` with your preferred configuration
    - For example:
      - `--license_mask=1`
      - `--user_language=11`
      - `--gpu="vulkan"`
      - `--mount_cache=true`
8.  Save and exit out of the file
9.  The config you set will now be applied to this specific game in Pegasus

#### Steam Shortcuts through Steam ROM Manager

1. Add your ROMs to Steam through Steam ROM Manager
2. On the game page in Steam, click the `Gear` icon, click `Properties`
3. In the `Launch Options` box, type `--CONFIGNAME=CONFIGVALUE`
   - For example:
     - `--license_mask=1`
     - `--user_language=11`
     - `--gpu="vulkan"`
     - `--mount_cache=true`
4. The config you set will now be applied to this specific game in Steam

---

### How to Access Xenia Settings in Game Mode

[Back to the Top](#xenia-table-of-contents)

If you added Xenia as a shortcut to Steam through the "Emulators" parser in Steam ROM Manager, you may notice that it launches into a black screen if you try to open it in Game Mode. This is a quirk of how Proton interacts with Game Mode. However, there is a workaround.

#### How to Access Xenia Settings in Game Mode

1. On the Xenia shortcut in Game Mode, press the `Controller` icon
2. Toggle `Enable Back Grip Buttons` if they are not already enabled
3. Select one of the four back buttons and bind it using sub-commands to one of the below keyboard shortcuts depending on which setting you would like to open in Xenia. For instructions on sub-commands, see [How to Bind Sub-Commands](#how-to-bind-sub-commands)
   - `Alt` + `F` = File
     - The "File" menu is used to launch games
   - `Alt` + `G` = CPU
   - `Alt` + `H` = GPU

#### How to Bind Sub-Commands

1. Click on one of the four back buttons, bind it to `Alt`
2. Click the `Gear` icon to the right of the button, click `Add sub command`
3. Bind it to the corresponding letter in the list above, [How to Access Xenia Settings in Game Mode](#how-to-access-xenia-settings-in-game-mode-1) depending on which setting you would like to open in Xenia

---

### How to Extract ISOs to the XEX Format

[Back to the Top](#xenia-table-of-contents)

If you have an Xbox 360 ISO and you would like to extract it to XEX, either for compression or for modding purposes, you can do so using `extract-xiso`, a tool bundled with EmuDeck. `extract-xiso` is typically located in `Emulation/tools/chdconv` and this path will be used for the below instructions. However if `extract-xiso` is not in this folder, it can also be found in `/home/deck/.config/EmuDeck/backend/tools/chdconv`. If `extract-xiso` is in neither of these folders, you may need to re-install EmuDeck (uninstalling first **is not** necessary).

1. In Desktop Mode, open the `Emulation/tools/chdconv` folder
2. If you are not comfortable with a terminal, copy `extract-xiso` to `Emulation/roms/xbox360/roms`
   - If you are comfortable with a terminal, right click anywhere in `Emulation/tools/chdconv`, click `Open Terminal Here`, type `./extract-xiso "/PATH/TO/ROM"`
3. In `Emulation/roms/xbox360/roms`, right click anywhere, click `Open Terminal Here`
4. Type `./extract-xiso "NAMEOFROM"`
   - The quotes are required for the ROM name. Alternatively, you can type the first few letters of the ROM name, press `Tab` on a keyboard, and the terminal will automatically escape the rest of the name
5. Wait for it to finish extracting
6. A folder matching your ROM name will be created containing a `default.xex` file which can be used to launch the ROM

---

### How to Convert Xbox Live Arcade ROMs to XEX

[Back to the Top](#xenia-table-of-contents)

If you have an Xbox 360 ISO and you would like to extract it to XEX, either for compression or for modding purposes, you can do so using the Xenia GUI.

1. In Desktop Mode, open Xenia
2. In the top left, click `File`, `Install Content`, and navigate to your Xbox Live Arcade ROM
3. The game will be installed to the `Emulation/roms/xbox360/content` folder to a folder matching the Game ID of the game
4. The folder will contain a `default.xex` file which can be used to launch the ROM

---

### How to Compress ROMs to ZAR

[Back to the Top](#xenia-table-of-contents)

ZAR is a newer file format created by the Cemu developers allowing for optimized file storage. In a recent update, Xenia added support for ZAR allowing users to compress Xbox 360 ROMs.

As an example, `Banjo-Kazooie - Nuts & Bolts` in the ISO file format was 7.3 GB. When compressed, `Banjo-Kazooie - Nuts & Bolts` was 4.8 GB in the ZAR file format.

If you are using ISOs, first extract your ISOs to XEX. For instructions, see [How to Extract ISOs to the XEX Format](#how-to-extract-isos-to-the-xex-format). For Xbox Live Arcade ROMs, see [How to Convert Xbox Live Arcade ROMs to XEX](#how-to-convert-xbox-live-arcade-roms-to-xex).

1. In Desktop Mode, open Xenia
2. In the top left, click `Zar Package`, `Create`, and navigate to the folder containing your `default.xex` file
3. Select the destination for your ZAR file
4. Wait, there may not be any response from the application for several minutes depending on how large your original file is
5. Once it is complete, a ZAR file will be located in the directory you selected in Step 3

---

### How to Optimize Sonic Unleashed

[Back to the Top](#xenia-table-of-contents)

This section is a heavily modified version of the section from [THE DEFINITIVE STEAM DECK SONIC DOC](https://docs.google.com/document/d/1FsjXbyYQTIK9f9P_NYHoLGnv8_ZqHjgLPf9Qm0VMcVo/edit#heading=h.cropilw5ikhb).

This section will assume you have installed and configured Xenia through EmuDeck. For instructions on how to install Xenia through EmuDeck, see [How to Download Xenia](#how-to-download-xenia).

1. Extract Sonic Unleashed using the instructions in [How to Extract ISOs to the XEX Format](#how-to-extract-isos-to-the-xex-format)
2. Install Xenia through EmuDeck
   - For instructions, see [How to Download Xenia](#how-to-download-xenia)
   - EmuDeck will automatically download the patches folder and create a `portable.text` file. You do not need to add Xenia as a non-Steam game. If you would like to add Xenia to Steam, you may do so using the `Emulators` parser in Steam ROM Manager
3. In `Emulation/roms/xbox360`, right click `xenia-canary.config.toml`, click `Open with Kate` or a text editor of your choice
4. Change `max_queued_frames` to `16`, change `vsync` from `True` to `False`
   - The Google Doc also suggests you use `Vulkan`, however `D3D12` been massively improved in the year since the Google Doc was written. It is recommended you use `D3D12` first and only try `Vulkan` if `D3D12` does not work as expected
   - It may not be necessary to change `Vsync` or `max_queued_frames`, these are directly copied from the Google Doc. It is recommended you test these and see if these are required
5. In `Emulation/roms/xbox360/patches`, right click `53450812 - Sonic Unleashed.patch.toml`, click `Open with Kate` or a text editor of your choice. For each patch you would like to enable, change `is_enabled = false` to `is_enabled = true`
   - (Optional)
     - `60 FPS`
   - (Highly Recommended)
     - `Disable Color Adjustment`
     - `Disable Shadow Maps`
6. The remainder of the Google Doc covers how to apply the "AMD Grass Explosion Fix" using the Unleashed Mod Manager. At this point, it is recommended you first test the game to test the performance. If you would like to apply the "AMD Grass Explosion Fix", proceed to the [Unleashed Mod Manager](#unleashed-mod-manager) section

??? tip "Vertex Explosions"

    If you are seeing vertex explosions, bind F5 to L4/R4/L5/R5 (the back bumpers). While in game, press the respective button to clear the GPU cache. You may be required to press this button from time to time while playing Sonic Unleashed.

#### Unleashed Mod Manager

##### Lutris

1. In Desktop Mode, open Konsole
2. Enter:
   - `mkdir -p $HOME/Games/Lutris/UnleashedModManager/pfx`
   - This command will create a couple of **empty** folders to make managing and installing the patcher easier
3. Download UnleashedModManager, [https://github.com/hyperbx/Unleashed-Mod-Manager/releases/tag/1.12](https://github.com/hyperbx/Unleashed-Mod-Manager/releases/tag/1.12) to `/home/deck/Games/Lutris/UnleashedModManager`
   - Download `latest.zip`
4. Right click `latest.zip`, click `Extract`, `Extract Archive Here`
   - If the `.zip` creates a subfolder, move the contents out directly into `/home/deck/Games/Lutris/UnleashedModManager`
5. In Desktop Mode, open Discover and download Lutris
6. Click the `Wine` button on the left, click the little page icon to the right, download `wine-ge-8-26`
7. Click the `+` button in the top left of the Lutris application
8. Click `Add locally installed game`
   - On the `Game Info` tab:
     - Name: Unleashed Mod Manager
     - Sort Name: Leave Blank
     - Runner: Wine (Runs Windows games)
     - Release Year: Leave Blank
   - On the `Game Options` tab:
     - Executable: Click the `Browse` button and navigate to the `Unleashed Mod Manager.exe` file in `/home/deck/Games/Lutris/UnleashedModManager`
     - Arguments: Leave Blank
     - Working Directory: Leave Blank
     - Wine Prefix: Click the `Browse` button and select the `/home/deck/Games/Lutris/UnleashedModManager/pfx`
   - On the `Runner options` tab:
     - Wine version: `wine-ge-8.26-x86_64`
     - Leave everything else at defaults
9. Click the `Save` button in the top right
10. To open the patcher, open Lutris, select the UnleashedModManager tile, and click `Play`

##### Applying the AMD Grass Explosion Fix

1. In `Emulation/roms/xbox360`, create a `mods` folder
2. Download the AMD Grass Explosion Fix, [https://gamebanana.com/mods/download/393182#FileInfo_840774](https://gamebanana.com/mods/download/393182#FileInfo_840774) to the `Emulation/roms/xbox360/mods` folder
3. Right click `amd_grass_fix.7z`, click `Extract archive here`
4. Open `Unleashed Mod Manager.exe` through Lutris
   - Mods Directory: `Emulation/roms/xbox360/mods`
   - Game Executable: The `default.xex` file in the folder wherever you extracted your Sonic Unleashed ISO
   - Emulator Executable: `Emulation/roms/xbox360/xenia_canary.exe`
5. Click `Continue`, click `Refresh Mods List` and the `AMD Grass Explosion Fix` will appear
6. Check the mod, click `Save checked mods`, and it will now be applied to Sonic Unleashed
7. Uncheck `Uninstall mods automatically`

---
