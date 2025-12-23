# Adrian's dotfiles
This is the repository for my dotfiles for Sway, forked from [Flipe Facundes](https://github.com/felipefacundes/dotfiles).

## Dependencies
The dotfiles configuration references a lot of packages that may not be installed on your system:

```
swayfx swayidle swaybg waybar rofi wlrctl cliphist lights ly kwalletd6 rofi-power-menu grim wl-clipboard xorg-xprop libpulse dunst
```

# SwayWM
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/bf0b98b5-8246-4737-bcf2-cf37287cc7b1" />

## Changing language
This is not a tutorial on changing your system language, this will only change the language of the configuration strings.

In `.config/sway/config` replace XX from the line `import strings_XX` to a language code matching a language file in that same directory. 

## Autostart applications
Edit `.config/sway/startup` and add `exec yourapplication`.

## Keyboard Shortcuts
### Window management
- `Super+Shift+[Arrow Keys]` Move windows
- `Super+Shift+Q` Close window
- `Ctrl+Alt+Esc` Kill window
- `Super+Tab` Toggle floating window for selection
- `Alt+Tab` Toggle focus between floating and tiling windows
- `Super+Shift+C` Move window to center
- `Super+F` Toggle fullscreen mode
- `Super+S` Layout toggle split
- `Super+W` Layout toggle tabbed
- `Super+A` Layout toggle stacked
- `Super+Shift+[Arrow Keys]` Move window to workspace
In .config/sway/config replace XX from the line import strings_XX to a language code matching a language file in that same directory.
#### Resize mode
- `Super+R` Enter resize mode
- `Esc`/`Return` Exit resize mode
- `[Arrow Keys]` Resize window

### Window Navigation
- `Super+[Arrow Keys]` Navigate through windows
- `Super+[Number Keys]` Navigate through workspaces
- `Super+D` Go back and forth on workspaces

### Cursor navigation
- `Super+Equal`/`Super+Next` Right mouse button click
- `Super+Minus`/`Super+KP_7` Left mouse button click
- `Super+Ctrl+[Arrow Keys]` Move cursor

### Media
- `XF86AudioRaiseVolume` (volume up button) raises volume
- `XF86AudioLowerVolume` (volume down button) lowers volume
- `XF86AudioMute` (mute button) mutes the volume
- `Super+P` Opens volume control (pavucontrol)
- `XF86MonBrightnessUp` (brightness up button) raises brightness
- `XF86MonBrightnessDown` (brightness down button) lowers brightness
- `XF86ScreenSaver` (screen saver button) set brightness to 0
- `Alt+Space` Pause media playback

### Applications
- `Super+Space` Application launcher (Rofi)
- `Super+Enter` Terminal (Alacritty)
- `Ctrl+Esc` Task manager (HTOP)
- `Ctrl+Super+F` Web browser (Floorp)
- `Super+E` File explorer (xdg-open)
- `Print` Select screen area to save to clipboard
- `Ctrl+Print` Saves a full screenshot to clipboard
- `Ctrl+Shift+Print` Saves a full screenshot to `${HOME}/Pictures/Capture/${date + "%Y-%m-%d %H:%M:%S"} - Capture.png`)
- `Ctrl+Alt+R` OBS Studio

### System
- `Ctrl+L` Lock with swaylock
- `Ctrl+Shift+L` Power options (Rofi)
- `Ctrl+Shift+Alt+Delete` Power off
- `Super+U` System update (`pacman -Syu`)
- `Super+Ctrl+R` Reload Sway
- `Super+Shift+E` Exit Sway
- `Ctrl+Super+Q` Kill Sway
- `Alt+Apostrophe` Change audio output

# ly display manager
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/5e8a8ab3-e872-4a85-b248-202ba8d9a36b" />

You can also replace your display manager with ly, a TUI display manager. The config file in `.config/ly/` will not work, you have to copy it to `/etc/ly/config.ini` after installing the package `ly` and enabling the systemd service (also, disable your current DM).
