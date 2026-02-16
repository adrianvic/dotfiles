# Adrian's dotfiles
This is the repository for my dotfiles for Sway, forked from [Flipe Facundes](https://github.com/felipefacundes/dotfiles).

## Dependencies

> [!IMPORTANT]
> This dotfile has configuration specific to SwayFX, if you're using Sway, please comment out the configuration section used by SwayFX.

The dotfiles configuration references a lot of packages that may not be installed on your system:

```
swayfx swayidle swaybg waybar rofi wlrctl cliphist lights ly kwalletd6 rofi-power-menu grim wl-clipboard xorg-xprop libpulse dunst rofi-pulse-select soteria keepmenu python-pykeepass ydotool
```

<details>
  <summary>Dependency table</summary>

| Name              | Reason                                                                                                            |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| swayfx            | Window manager ¯\_(ツ)_/¯                                                                                         |
| swayidle          | Puts your computer to sleep after certain amount of time.                                                         |
| swaybg            | Wallpaper util                                                                                                    |
| waybar            | Status bar                                                                                                        |
| rofi              | Application/power menu, also used for switching audio in/outputs and accessing KeePass DBs.                       |
| wlrctl            | Moving the cursor with keyboard keybinds.                                                                         |
| cliphist          | Waybar's "[Clipboard]" button uses to show clipboard history.                                                     |
| lights            | Backlight control                                                                                                 |
| ly                | Login screen                                                                                                      |
| kwalletd6         | Keyring                                                                                                           |
| rofi-power-menu   | Power options provider for Rofi                                                                                   |
| grim              | Used to select screen sections for screenshots, only needed for selection screenshot.                             |
| wl-clipboard      | Provides control over Wayland clipboard.                                                                          |
| xorg-xprop        | Used to set XWayland display scale.                                                                               |
| libpulse          |                                                                                                                   |
| dunst             | Delivers notifications, some apps (Electron-based) will hang when you receive a notification if it's not present. |
| rofi-pulse-select | Provides audio in/output for Rofi.                                                                                |
| soteria           | Polkit, asks for elevation when needed. Akin to Windows' ACL.                                                     |
| keepmenu          | KeePass provider for Rofi                                                                                         |
| python-pykeepass  | Dependency of KeepMenu                                                                                            |
| ydotool           | KeepMenu uses this to type passwords.                                                                             |

</details>

# SwayWM
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/bf0b98b5-8246-4737-bcf2-cf37287cc7b1" />

## Changing language
This is not a tutorial on changing your system language, this will only change the language of the configuration strings.

In `.config/sway/config` replace XX from the line `import strings_XX` to a language code matching a language file in that same directory. 

## Autostart applications
Edit `.config/sway/startup` and add `exec yourapplication`.

## Keyboard Shortcuts
<details>
  <summary>Default modifiers</summary>

- `Mod` is Super by default.
- `Menu` is the context menu button, generally only present in full-size keyboards.

</details>

### Window management
- `Mod+Shift+[Arrow Keys]` Move windows
- `Mod+Shift+Q` Close window
- `Ctrl+Alt+Esc` Kill window
- `Mod+Tab` Toggle floating window for selection
- `Alt+Tab` Toggle focus between floating and tiling windows
- `Mod+Shift+C` Move window to center
- `Mod+F` Toggle fullscreen mode
- `Mod+S` Layout toggle split
- `Mod+W` Layout toggle tabbed
- `Mod+A` Layout toggle stacked
- `Mod+Shift+[Arrow Keys]` Move window to workspace
In .config/sway/config replace XX from the line import strings_XX to a language code matching a language file in that same directory.

#### Resize mode
- `Mod+R` Enter resize mode
- `Esc`/`Return` Exit resize mode
- `[Arrow Keys]` Resize window

### Window Navigation
- `Mod+[Arrow Keys]` Navigate through windows
- `Mod+[Number Keys]` Navigate through workspaces
- `Mod+D` Go back and forth on workspaces

### Cursor navigation
- `Mod+Equal`/`Mod+Next` Right mouse button click
- `Mod+Minus`/`Mod+KP_7` Left mouse button click
- `Mod+Ctrl+[Arrow Keys]` Move cursor

### Media
- `XF86AudioRaiseVolume` (volume up button) raises volume
- `XF86AudioLowerVolume` (volume down button) lowers volume
- `XF86AudioMute` (mute button) mutes the volume
- `Mod+P` Opens volume control (pavucontrol)
- `XF86MonBrightnessUp` (brightness up button) raises brightness
- `XF86MonBrightnessDown` (brightness down button) lowers brightness
- `XF86ScreenSaver` (screen saver button) set brightness to 0
- `Alt+Space` Pause media playback

### Applications
- `Mod+Space` Application launcher (Rofi)
- `Mod+Enter` Terminal (Kitty)
- `Mod+Esc` Task manager (HTOP)
- `Ctrl+Mod+F` Web browser (Floorp)
- `Mod+E` File explorer (xdg-open)
- `Print` Select screen area to save to clipboard
- `Ctrl+Print` Saves a full screenshot to clipboard
- `Ctrl+Shift+Print` Saves a full screenshot to `${HOME}/Pictures/Capture/${date + "%Y-%m-%d %H:%M:%S"} - Capture.png`)
- `Ctrl+Alt+R` OBS Studio

#### KeePass
- `Menu` Access loaded KeePass DB (if not loaded it will prompt for the DB directory, use the shortcut below to open the default DB)
- `Mod+Menu` Load and open default DB (defined in the config)

### System
- `Ctrl+L` Lock with swaylock
- `Ctrl+Shift+L` Power options (Rofi)
- `Ctrl+Shift+Alt+Delete` Power off
- `Mod+U` System update (`pacman -Syu`)
- `Mod+Ctrl+R` Reload Sway
- `Mod+Shift+E` Exit Sway
- `Ctrl+Mod+Q` Kill Sway
- `Alt+Apostrophe` Change audio output (sink)
- `Alt+Shift+Apostrophe` Change audio input (source)

# ly display manager
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/5e8a8ab3-e872-4a85-b248-202ba8d9a36b" />

You can also replace your display manager with ly, a TUI display manager. The config file in `.config/ly/` will not work, you have to copy it to `/etc/ly/config.ini` after installing the package `ly` and enabling the systemd service (also, disable your current DM).
