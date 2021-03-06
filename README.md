# i3 configuration to play well with KDE Plasma Desktop

Note: I also posted it 
[here](https://www.reddit.com/r/unixporn/comments/7vm0su/i3_plasma_ive_been_running_this_for_a_while/) 
with a relevant and up to date screenshot.

## Install:

### Make i3 the default window manager for KDE

First you have to create the `i3` launcher:

```
echo "export KDEWM=/usr/bin/i3" > ~/.config/plasma-workspace/env/set_window_manager.sh

```

Then you have to start (or restart) KDE by choosing "KDE Plasma Desktop" in
your login screen, if you have one.

I would try it with an empty `i3` configuration first, see if it works
properly, then proceed to installing the configuration.

### Install the configuration

1. Clone this repo: `git clone https://github.com/nightsh/i3-plasma.git $HOME/.i3-plasma`
2. Make sure you have:
  * a `$HOME/.local/bin` directory: `mkdir -p $HOME/.local/bin`
  * a `$HOME/.i3` directory: `mkdir -p $HOME/.i3`
3. Symlink:
  * the config: `ln -s $HOME/.i3-plasma/config $HOME/.i3/`
  * the scripts: `ln -s $HOME/.i3-plasma/.local/bin/* $HOME/.local/bin/`
4. Start or restart `i3`


## Requirements

Recommended software used in the config / scripts:

* nitrogen (for wallpaper)
* fswebcam (for `camshot` script)
* synclient (for `toggle_touchpad` script)
* xcompmgr (for compositing)
* custom lock screen needs:
  * i3lock
  * scrot
  * convert (imagemagick)


KDE things:

* spectacle
* konsole
* dolphin
* kcalc


Misc software:

* chromium / firefox
* emacs / nvim
* thunderbird
