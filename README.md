# fdf3-tate
THRotator-style tate mod for Touhou Makuka Sai ~ Fantastic Danmaku Festival Part III

## Installation
1. Download the latest release zip.
2. Extract the zip into the game folder, next to `THMHJ.exe` (Steam: right-click the game > Manage > Browse local files).

### Linux / Proton
Also set the Steam launch options to:
```
WINEDLLOVERRIDES="dxgi=n,b" %command%
```

## Hotkeys (in game)
| Keys | Action |
|---|---|
| Alt+Left | Rotate clockwise |
| Alt+Right | Rotate counterclockwise |
| Alt+Up | Force HUD layout |
| Alt+Down | Force whole screen |
| Alt+0 | Settings menu (Save writes `fdf3-tate.ini`) |

## How it works
- Gameplay is detected from the HUD labels (yellow Hi-score, pink Life): HUD layout in game, whole screen in menus.
- Dialog scenes switch to the whole screen. Turn off **Whole screen during dialog** in the Alt+0 menu to keep the HUD layout during dialog.
- The difficulty text is auto-scaled to fill its box, so short ones (HARD) show big and EX-ULTIMATE still fits.
- Portrait or 4:3 desktops: the game window is kept covering the screen (windowed or fullscreen both work). Keep rotation at 0 if the desktop itself is rotated.
- CRTs / stretched screens: set **Screen shape** in the Alt+0 menu (Display) to the screen's real shape.
- If something breaks, check `fdf3-tate-log.txt` in the game folder.

## Notes
- As of now, from my testing, SpecialK does not work with this mod. I may try to fix it in the future.

## Building
Install mingw-w64, then run `./build.sh` (makes `dxgi.dll`):
- Arch / Artix: `sudo pacman -S mingw-w64-gcc`
- Debian / Ubuntu: `sudo apt install g++-mingw-w64-x86-64`
- Fedora: `sudo dnf install mingw64-gcc-c++`

## Credits
- Inspired by [THRotator](https://github.com/massanoori/THRotator)
- Settings menu uses [Dear ImGui](https://github.com/ocornut/imgui) (MIT license, see `imgui/LICENSE.txt`)
