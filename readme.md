## Requirements

* Copy your default pipewire.conf from `/usr/share/pipewire/` to `~/.config/pipewire/`
* Copy the contents of pipewire.conf from this repository and paste them inside `content.exec = []` located at the end of your pipewire.conf ![image](https://user-images.githubusercontent.com/77363063/172093587-3a62f1ed-e8be-4800-8791-cc1c1912eb51.png)
* Restart pipewire.service using `systemctl --user restart pipewire.service`
* Done

## How to use

* Open app with video/music playing and open pavucontrol
* Open the playback tab inside pavucontrol and select 'app' from the dropdown menu for the channel who's audio you want to be shared (Firefox in this example)![image](https://user-images.githubusercontent.com/77363063/172094382-ee3e5735-8181-4421-8459-471eeffe7e82.png)
* Now open the recording tab, and select 'mic+app' for the channel you want to share your app audio + mic to (Discord in this example)![image](https://user-images.githubusercontent.com/77363063/172094811-6d4c8649-5c42-4c31-8e71-57708d634ce7.png)
* Done
