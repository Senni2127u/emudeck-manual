# <img src="/assets/emulators/srm.png" alt="EmuDeck guide" width="50" style="vertical-align: middle"> Steam Rom Manager (SRM)

Allows you to add your ROMs directly to your library as if they were Steam Games.

!!! warning "Installation"

    Since SRM can be hard to use it will only be installed in *Custom Mode* or through ==Manage Emulators==

!!! info "Number of games"

    If you have a lot of ROMS it's recommended to use ES-DE instead of SRM

### Launching SRM

=== "Linux / SteamOS"

    You need to be in Desktop mode and launch the EmuDeck app, once it's open you can launch SRM to add games by opening the EmuDeck App and selecting ==Steam ROM Manager== in the left sidebar.

=== "Windows"

    Launch the EmuDeck app, once it's open you can launch SRM to add games by opening the EmuDeck App and selecting ==Steam ROM Manager== in the left sidebar.

    !!! info "Slow to launch"

        While in Linux / SteamOS loads almost instantly, in Windows SRM can take several seconds to launch, please be patient.

### Adding Games

<iframe width="800" height="450" src="https://www.youtube-nocookie.com/embed/BsqWFHPp5UU" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"></iframe>

SRM works by using parsers, every system has it's own parser, every parser will detect all your games

- Activate / deactivate your parsers by clicking on them. Some systems can be emulated with more than one emulator, so make sure you don't have duplicated parsers selected.

- Click on ==Add Games==, read the instructions and then hit the ==Parse== button.

- SRM will now start finding your games and downloading its artwork, wait until the message ==Retrieving urls== at the top is gone.

- Click on ==Add to Steam== and wait until you get a notification in the top right saying it has finished.

- Now you can go to _Game Mode / Big Picture_ and you'll find your games organised by systems in the ==Collections== tab

!!! info "Add more games later"

    You need to follow the previous steps every time you want to add new games, it's recommended to only select the parser of the system you are going to add games.

!!! bug "My games are not showing in SRM"

    If your games are not appearing it could be because you are using subfolders or an incorrect file format. Inside every rom folder you have a ==systeminfo.txt== file that describes the formats your ROMS needs to be.
