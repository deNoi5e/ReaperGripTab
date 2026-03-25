# GripTab 🎸

> Real-time MIDI to Guitar Tablature for REAPER DAW

GripTab is a REAPER ReaScript that reads MIDI items and displays them as live guitar tablature in a floating window — with playhead cursor, proportional timing, zoom, and 10 tuning presets.

![GripTab Screenshot](https://raw.githubusercontent.com/deNoi5e/ReaperGripTab/main/screenshot.png)

---

## Features

- 🎵 **Live tablature** — tab updates instantly when you select a MIDI item
- ▶️ **Playhead cursor** — follows REAPER playback in real time, auto-scrolls
- ⏱️ **Proportional spacing** — pauses between notes shown as empty space
- 🎸 **10 tuning presets** — Standard, Drop D, Open G, Open D, Open E, Open A, DADGAD, Half-step down, Full-step down, Drop C
- 🔍 **Zoom** — `+` / `-` keys or `Ctrl + mouse wheel`
- 🖱️ **Scroll** — arrow keys or mouse wheel
- 🤚 **Smart fingering** — notes are spread across strings in comfortable hand positions, not piled on one string

---

## Installation

### Via ReaPack (recommended)

1. In REAPER open **Extensions → ReaPack → Import repositories…**
2. Paste this URL:
   ```
   https://raw.githubusercontent.com/deNoi5e/ReaperGripTab/main/index.xml
   ```
3. Click **OK**, then go to **Extensions → ReaPack → Browse packages**
4. Find **GripTab** in the **MIDI** category → **Install**
5. Restart REAPER when prompted

### Manual installation

1. Download [`GripTab.lua`](https://github.com/deNoi5e/ReaperGripTab/raw/main/GripTab.lua)
2. Copy it to your REAPER Scripts folder:
   ```
   %APPDATA%\REAPER\Scripts\
   ```
3. In REAPER open **Actions → Show action list → Load…**
4. Select `GripTab.lua` and assign it to a shortcut or toolbar button

---

## Usage

1. **Select a MIDI item** in the Arrange view
2. **Run GripTab** from the Actions list (or your assigned shortcut)
3. A floating tablature window appears

### Controls

| Key / Action | Function |
|---|---|
| `←` `→` or mouse wheel | Scroll tablature |
| `+` / `=` | Zoom in |
| `-` | Zoom out |
| `Ctrl` + mouse wheel | Zoom in/out |
| `A` | Toggle auto-scroll during playback |
| Click **Tuning ▾** button | Open tuning preset selector |
| `Esc` | Close window |

### Tuning presets

| Preset | Strings (low → high) |
|---|---|
| Standard | E A D G B e |
| Drop D | D A D G B e |
| Open G | D G D G B D |
| Open D | D A D F# A D |
| Open E | E B E G# B E |
| Open A | E A E A C# E |
| DADGAD | D A D G A D |
| Half-step down | Eb Ab Db Gb Bb eb |
| Full-step down | D G C F A d |
| Drop C | C G C F A D |

---

## Requirements

- **REAPER** 6.0 or later (reaper.fm)
- No additional plugins or extensions needed

---

## Building from source

The distributed `GripTab.lua` is compiled Lua 5.4 bytecode. To build from source:

### Prerequisites
- [Lua 5.4](https://luabinaries.sourceforge.net/) — `luac.exe` must be available
- PowerShell 5+

### Build
```powershell
git clone https://github.com/deNoi5e/ReaperGripTab.git
cd ReaperGripTab
# Source files are not included in this repo (closed source)
```

> **Note:** Source code is not publicly distributed. The compiled script is free to use.

---

## Changelog

### 1.0.0 — 2026-03-25
- Initial release
- MIDI to guitar tab rendering via REAPER `gfx` API
- 10 tuning presets with live switching
- Real-time playhead cursor with auto-scroll
- Proportional note spacing (pauses visible)
- Smart fingering algorithm (hand position window, minimises fret spread)
- Zoom and scroll controls

---

## License

© 2026 deNoi5e. All rights reserved.  
This script is free to use but not open source. Redistribution or modification without permission is prohibited.

---

## Links

- [REAPER](https://www.reaper.fm/)
- [ReaPack](https://reapack.com/)
