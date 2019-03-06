# Better Linux Mint Terminal (with ST)

The [suckless terminal (st)](https://st.suckless.org/) with some additional features:

+ Linux Mint Theme
+ Adjustable transparency/alpha
+ Compatibility with `Xresources` and `pywal` for dynamic colors
+ Copy to clipboard (ctl-shift-c)
+ Default font is system "mono" at 14pt, meaning the font will match your system font.
+ Hold alt and press either ↑/↓ or the vim keys k/j to move up/down in the terminal.
+ Shift+Mouse wheel will as well.
+ Alt-u and Alt-d scroll back/forward in history a page at a time.
+ Alt-PageUp and Alt-PageDown will do the same.
+ Zoom in/out with Alt+Shift+k/j or u/d for larger intervals.
+ Vertcenter

## Prequisite
`make fontconfig libX11 LibXft libxres`

## Install

```
make
sudo make install
```

## Need a Desktop Menu
```
sudo touch /usr/share/applications/simple-terminal.desktop
sudo -E vim /usr/share/applications/simple-terminal.desktop
```
    [Desktop Entry]
    Name=Simple Terminal
    GenericName=Terminal
    Comment=standard terminal emulator for the X window system
    Exec=st -t "Mint"
    Terminal=false
    Type=Application
    Encoding=UTF-8
    Icon=utilities-terminal
    Categories=System;TerminalEmulator;
    Keywords=shell;prompt;command;commandline;cmd;GTK;GNOME;Utility;

## Usage
```
usage: st [-aiv] [-c class] [-f font] [-g geometry] [-n name] [-o file]
          [-T title] [-t title] [-w windowid] [[-e] command [args ...]]
```
    # st -t "Suckless Terminal" -f "Source Code Pro:style=Semibold:size=12" -g "80x24"
