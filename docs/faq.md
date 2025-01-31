# :material-chat-question: Frequently Asked Questions

[TOC]

### How do I open the various emulators and tools in Desktop Mode?

=== "SteamOS / Linux"

    EmuDeck will create a link for each emulation in the Games section of your Applications Launcher

=== "Windows"

    EmuDeck will create a link for each emulation in an EmuDeck folder in your Start Menu

**Note:**

- Flatpaks can also be updated and managed through Discover.
- AppImages, Binaries, and Cemu can be updated through the `Manage Emulators` section of the EmuDeck application.

Here's how to open everything in Desktop Mode:

---

### Why is EmuDeck not downloading?

Internet issues are an increasingly common issue among Steam Decks, even if your internet works perfectly fine on other devices, or you have the latest and fastest internet. You may notice that EmuDeck isn't installing properly, or is taking a long time time to install. You may notice these same internet issues when you try to browse the internet or download a game and the internet speeds are much slower than you would expect.

You can fix these issues by adjusting your DNS, in System Settings within Desktop Mode, in `Configure Network Settings`.

**Note:** If you are noticing unexpected behavior with RetroAchievements causing errant controls or freezing, consider trying the below steps.

**Here's How:**

1. Click the bottom left icon in the taskbar (Steam Deck icon), click `Settings` in the list, open `System Settings`.
2. Click `Connections` on the left.
3. On the `IPv4` tab, change the `Method` to `Automatic (Only Addresses)`.
4. In the `DNS Servers` box, enter `1.1.1.1`.
5. Click the `IPv6` tab at the top, change the `Method` to `Disabled`.
6. For good measure, restart your Steam Deck.

**Note:** If the above steps still do not fix the issue for you, you can try switching to a 2.4 GHz WiFi network if your ISP provides you with one.

---

### Which emulators require BIOS files or firmware?

Refer to [The EmuDeck Cheat Sheet](../../cheatsheet.md) for a list of required BIOS files.

---

### What are the expected file types for the various emulators?

Refer to [The EmuDeck Cheat Sheet](../../cheatsheet.md) for a list of the expected file types.

---

### If I install EmuDeck, will it clutter my Steam library?

No! EmuDeck is a "dumb" script that installs a suite of tools and emulators to your Steam Deck. One tool that EmuDeck installs is "Steam ROM Manager", a tool that allows you to add ROMs as non-Steam game shortcuts to your library. You are not required to use Steam ROM Manager.

EmuDeck also installs ES-DE, a front-end that manages all of your ROMs within a single app. You may choose to use either Steam ROM Manager, ES-DE, both, or neither of them. EmuDeck is simply a script, and how you choose to use its installed suite of tools and emulators is up to you.

After you have installed EmuDeck, you can use Steam ROM Manager and select which parsers you would like to use. You can use the `ES-DE` parser and the `Emulators` parser to add ES-DE and EmuDeck's installed suite of emulators to your Steam library. Adding emulators to your library allows you to tweak settings directly in Game Mode. Turning on other parsers will add the respective system's ROMs to your library. Learn how to generate and save an app list here: [How to Generate and Save an App List](../../tools/steamos/steam-rom-manager.md#how-to-generate-and-save-an-app-list).

**Read:** [What does EmuDeck Install?](#what-does-emudeck-install), for a list of the tools and emulators EmuDeck installs.

**Read:** [Steam ROM Manager](../../tools/steamos/steam-rom-manager.md) for more information on Steam ROM Manager.

**Read:** [ES-DE](../../tools/steamos/es-de.md) for more information on ES-DE.

---

### How do I update EmuDeck and emulators?

When opening the EmuDeck app, the app itself will autoupdate if necessary. _This won't touch your current installation, settings or games_.

## You can update the emulators from Manage Emulators

### How do I choose which emulators to install?

You can run EmuDeck in `Custom Mode` for more granular options, including a prompt that allows you to select which emulators you would like to install.

---

### How do I change the Steam Input Controller Profile?

#### Preface

EmuDeck comes with a few Steam Input profiles to make hotkeys easier to use in a few emulators. If an emulator does not have a Steam Input Profile, make sure you're on `Gamepad with Joystick Trackpad`, otherwise some controls may not work.

EmuDeck comes with Steam Input Profiles for the following emulators:

- Cemu
  - The Steam Input Profile is necessary to switch screens
- Citra
  - The Steam Input Profile is necessary to switch screens
- DuckStation
- melonDS
- mGBA
- PPSSPP
- RMG

#### Changing Steam Input Profiles

In Game Mode, single click the game you would like to change the Steam Input Profile for, and click the `Controller Icon` on the right of the screen. Click the layout (whatever name it is currently set to) at the top, and you will see a drop-down menu. When playing a PSX, 3DS, or Wii U Game, switch to the respective Steam Input Profile.

For a visual, watch the following GIF (DuckStation is being used as an example):

<img src="https://user-images.githubusercontent.com/108900299/194612525-670e56a1-a16a-4dbf-a03f-85d14e7f7b76.gif?raw=true"/>

---

### Why is my emulator or game muted?

There is no one known reason why an emulator or ROM (run through an emulator) can accidentally be muted. However, the fix is simple.

**Tutorial**

1. In Desktop Mode, open the emulator
   - Example: If you are playing a PS2 ROM, open PCSX2
2. Either temporarily turn off the `Start in Fullscreen` feature or make sure you have a way to use `Alt` + `Tab`
   - You can bind `Alt` + `Tab` to a back bumper, plug in a keyboard, or use Anydesk to switch out of the emulator
3. Launch a game
4. In the taskbar, press the audio icon, select the `Applications` tab, in the list, you should see your emulator with a muted speaker icon
   - <img src="https://user-images.githubusercontent.com/108900299/216749000-600e9792-4f15-449f-9eaf-aba6bc0c6465.png" height="300">
5. Click the speaker icon to unmute the emulator
   - Make sure to turn fullscreen back on if you turned it off
6. This fix applies to any game you launch through that emulator

---

### For systems with multiple emulators, how do I select which emulator to use?

#### Steam ROM Manager

These systems will have multiple parsers, each corresponding to a different emulator or RetroArch core. For example: PSX can be played through DuckStation (Standalone), SwanStation, or Beetle PSX. If you prefer to use DuckStation (Standalone) for PSX, enable the Sony PlayStation - DuckStation parser and make sure the SwanStation and Beetle PSX parsers are disabled

#### ES-DE

These systems will have a set default. However, you can change which emulator or RetroArch core is used:

1. In ES-DE, press the Start button
2. Scroll down and select Other Settings
3. Select Alternative Emulators
4. Scroll down to the system you would like to configure, press B, and select your preferred emulator

---

---

## EmuDeck Tips and Tricks

---

### How do I find .var, .config, or any folder with a period in front?

=== "SteamOS/Linux KDE"

    1. Open Dolphin (the file manager with a folder icon).
    2. In Dolphin (the file manager), press the hamburger button in the top right, `☰`.
    3. Select `Show Hidden Files`.
    4. You should now see a handful of folders with reduced transparency, including `.var` and `.config`.

---

### How do I reset an emulator's configurations?

Sometimes after installing EmuDeck, you may notice an emulator's configurations were not set properly or you tweaked something on accident and you do not remember the default settings.

You may reset an emulator's configurations in the `Manage Emulators` page.

**Tutorial**

1. Open EmuDeck on your desktop.
2. Click the `Manage Emulators` button.
3. Select which emulator configurations you would like to reset in the drop-down menu.
4. Click `Reset configuration`, wait a moment.
5. Your selected emulator has been reset.

---

### How do I navigate to my SD Card through an emulator's menu?

For some emulators, you may need to navigate to your SD Card to install updates/DLC or locate a file of some sort for the emulator. On Linux, your SD card is a file path, so navigating there through the menu will look different.

**Using Yuzu as a Reference:**

1. Open Yuzu.
2. Click `Files`, `Install files to NAND`.
3. Click `Computer` on the left.
4. Your SD Card path is `/run/media/mmcblk0p1`.
   1. `mmcblk0p1` is the default name of the SD Card when formatted by the Steam Deck.
5. You will now see your `Emulation` folder and you can proceed to locate your files.

For some emulators, you may need to click `Other Locations` first before seeing `Computer`.

Visual Reference (Ryujinx):

- `Other Locations`, `Computer`: <img src="https://user-images.githubusercontent.com/108900299/197047851-c59bb1ce-f064-4111-8036-065799fbbfbd.png" height="300">
- `mmcblk0p1` (your SD Card): <img src="https://user-images.githubusercontent.com/108900299/197048116-4e762160-a5e0-48df-887c-24129123dffb.png" height="300">

Visual Reference (Yuzu):

- `Computer`: <img src="https://user-images.githubusercontent.com/108900299/197048223-941a5f71-39db-4262-b89a-444e892f057d.png" height ="300">
- `mmcblk0p1` (your SD Card): <img src="https://user-images.githubusercontent.com/108900299/197048383-1e2c7101-da86-4c33-8065-3f734fcfbdf9.png" height="300">

Visual Reference (Dolphin):

- `Other Locations`, `Computer`: <img src="https://user-images.githubusercontent.com/108900299/197048561-b791cd7f-34f9-4971-89a8-69c523098c6c.png" height="300">
- `mmcblk0p1` (your SD Card): <img src="https://user-images.githubusercontent.com/108900299/197048683-623c38ab-f2fd-4097-849a-77f62040a2d9.png" height="300">

Visual Reference (RPCS3):

- `rootfs`: <img src="https://user-images.githubusercontent.com/108900299/197050154-f026381f-093d-45c6-8fc3-e9674ee2f8dd.png" height="300">
- `mmcblk0p1` (your SD Card): <img src="https://user-images.githubusercontent.com/108900299/197050241-662e7d70-c99e-47e4-b6fe-13c51200a2db.png" height="300">

---

### Why are my emulators stuttering? How do I improve emulator performance?

There may be a number of reasons for this, but your first debugging tool should be to ensure that both the frame limiter and the refresh rate are off. Consider turning off half rate shading if you had it previously on. Half rate shading may cause visual glitches as well.

To find these options, press the QAM ("..." button), press the battery icon, press advanced view.

**Note:** It's a good idea to use per game profiles if you intend on changing any of these settings.

---

### How do I manage ROMs with multiple discs?

[How to Manage ROMs with Multiple Discs](../../file-management/steamos/file-management.md#how-to-manage-roms-with-multiple-discs)

---
