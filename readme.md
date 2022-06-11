 # Discord Screen Share Fix Audio on Linux

 No need too much bla-bla lets just get it over with.

 ## Requirements

 * `pulseaudio`: This thing is our savior. Usually comes pre-installed. If not then probably your system is using something else so better **not** use this script than breaking your system by replacing your current one with `pulseaudio`, this script is for `pulseaudio` only.
 * `pavucontrol-qt`: To configure input and output from mic and app into discord. Very useful tool for routing your audio.

 ## Setting Up

 Just run the script:
 ```sh
 ./discord-scrshrwa.sh
 ```
 `chmod +x` it first if it's not executable yet.

 And then boot up discord, hop in a VC and start streaming.
 It's that ez, so simple right.


 ## hol' up, _it's not done yet_

 Now you're _in a vc and streaming_ some hanime with no audio, your friends and gfs that are watching are complainin in the background as you're doing these:

 Open `pavucontrol-qt` and find your browser/game in `Playback` tab and set its playback on `app`,
 and then go to the `Recording` tab and find something like `WEBRTC VoiceEngine :recStream` and set its source to `Monitor of mic+app`.


 # Anddddddd Done

 Close (or don't) `pavucontrol-qt`.

 Go back to discord, _unmute_ yourself and continue your hanime and watch together with everyone, safe and sound.


 ## Tips

 * You can mute your mic in `pavucontrol-qt`.
 * Try setting discord input sensitivity to -100dB(or -99dB if you want the indicator to show when your audio is inactive) on discord settings.
 * If you wanna remove the virtual streams, run
 ```sh
 pactl unload-module <number>
 ```
 where `<number>` is one of the script's terminal output. Do it once for each number. If you forget the numbers, run
 ```sh
 pactl list
 ```
 and find the virtual streams number.

 * If discord ever prompt you to switch audio device, **don't switch!**
 * If you don't want to run the script every time you boot up your PC, copy the codes from the script (exclude the first line) and append it to your `/etc/pulse/default.pa`, make sure to remove the `pactl` prefix from each line.
 * There's `pavucontrol` which uses GTK, if you have display issue with `pavucontrol-qt` you might want to use that.

 # Issues

 * If discord crashes when streaming, ignore it. Try streaming again, usually only one time crash.

# Tested in
- Manjaro Linux (Arch)
- Ubuntu 20.04
