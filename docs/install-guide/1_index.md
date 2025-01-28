# :simple-turborepo: Installing EmuDeck Desktop

First of all download the appropriate installer for your system from emudeck.com, execute it and wait for the EmuDeck App to launch.

Once the app is installed you need to pick either [Easy Mode](# "Recommended for users new to Emulation") or [Custom Mode](# "Recommended for advanced users")

<img src="/assets/install_guide/easy_custom.png" alt="EmuDeck guide">

!!! question "Which option should I pick?"

    === "Easy"
        If you are new to Emulation this is the recommended method for you.

        EmuDeck will only let you customize where you want to store your ROMS and BIOS, everything else will be setup with our default settings. You can always change settings, add or remove emulators after the installation.

        <img src="/assets/install_guide/select-storage.png" alt="EmuDeck guide">

        After the installation is complete EmuDeck will ask you to setup cloud saves.


    === "Custom"
        EmuDeck will ask you several questions to customize your installation:

        - Location to store your ROMS and BIOS
        - Emulators to install
        - Configure RetroAchievements
        - Bezels for 4:3 and 1:1 systems
        - Aspect ratio for systems
        - Shaders for LCD / CRT simulation
        - Controller Layout
        - Level of integration: EmulationStation or SteamLibrary
        - CloudSaves

        After the installation is complete EmuDeck will ask you to setup cloud saves.

??? bug "Possible issues when installing"

    === "SteamOS / Linux"

        - **I can't select my SD Card**
            - Solution: Make sure your SD Card is formatted as EXT4. You can format it from Game Mode inside  ==Preferences -> Storage==
        - **EmuDeck never downloads**
            - Solution: Make sure you are using good Internet [DNS](# "DNS are responsible to resolve internet domains, bad DNS can make your internet connection unreliable and slow").

    === "Windows"

        - **I'm stuck on Collection Drives**
            - Solution: Make sure you have git installed, run the installer again to install it.

        - **EmuDeck never downloads**
            - Solution: Make sure you are using good Internet [DNS](# "DNS are responsible to resolve internet domains, bad DNS can make your internet connection unreliable and slow").

??? info "What's installing EmuDeck in my system?"

    === "SteamOS / Linux"

        - **Emulators**: EmuDeck will install emulators in ==$HOME/.var== in the case of [Flatpack](# "Flatpak is a framework for distributing desktop applications across various Linux distributions") Emulators and in  ==$HOME/Applications== in the case of [AppImage](# "AppImage is an open-source format for distributing portable software on Linux") Emulators.

        - **Settings**: All settings and additional software that EmuDeck needs to work will be created inside ==$HOME/.config/EmuDeck==

        - **Emulation folder**: EmuDeck will create an Emulation folder that will contain your ROMS and BIOS, this folder is created where the user selected on install.

    === "Windows"

        - **Emulators**: EmuDeck will install emulators in ==AppData/Roaming/EmuDeck/Emulators== so if you have emulators already installed it won't overwrite them.

        - **Settings**: All settings and additional software that EmuDeck needs to work will be created inside ==AppData/Roaming/EmuDeck/==

        - **Emulation folder**: EmuDeck will create an Emulation folder that will contain your ROMS and BIOS, this folder is created where the user selected on install.

??? info "What's inside the Emulation folder?"

    Inside Emulation you'll find these folders

    | Subfolder      | Description                          |
    | ----------- | ------------------------------------ |
    | `bios`       | Some Emulators need BIOS to work, this is where to place them  |
    | `hdpacks`       | HD Textures that some Emulators can use to improve the way games look |
    | `roms`    | Your ROMS go in here, it's populated with a subfolder for each system |
    | `saves`    | We store your saved games in this folder so it's easier to backup them if you need to |
    | `storage`    | Assets that some Emulators or EmulationStation DE store |
    | `tools`    | Some internal tools that EmuDeck uses |

<!--
## Video guides

!!! success "Pick your system"

    === "SteamOS / Linux"

         <iframe width="800" height="400" src="https://www.youtube-nocookie.com/embed/Y5r2WZAImuY" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"></iframe>

    === "Windows"

        <iframe width="800" height="400" src="https://www.youtube-nocookie.com/embed/05dunYi6hkY" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"></iframe> -->
