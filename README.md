# Tetris (Terminal Edition)

A classic Tetris clone that runs right in your terminal — colored blocks,
next-piece preview, scoring, and speed that ramps up as you level up.

## Download & run

1. Grab `tetris.exe` from the [Releases](../../releases) page
2. Double-click it, or run it from a terminal:
   ```
   tetris.exe
   ```
3. A window opens with the board — you're playing.

No installer, no extra files, nothing else to download. It's a single
`.exe` with everything built in.

## Controls

| Key                  | Action             |
|-----------------------|-------------------|
| `A` / `D` or ←/→      | Move left / right |
| `S` or ↓               | Soft drop         |
| `W` or ↑               | Rotate            |
| `Space`                | Hard drop         |
| `Q`                    | Quit              |

## Scoring

| Lines cleared at once | Points          |
|------------------------|----------------|
| 1                       | 40 × level    |
| 2                       | 100 × level   |
| 3                       | 300 × level   |
| 4 (Tetris!)             | 1200 × level  |

Your level goes up every 10 lines cleared, and the board speeds up each
level.

## Requirements

- Windows 10 (version 1511 or later) or Windows 11

That's it — the game draws its colors using a feature built into modern
Windows terminals, so there's nothing extra to install.

## Troubleshooting

**Windows warns "Windows protected your PC" / SmartScreen blocks it.**
This happens with any unsigned `.exe` downloaded from the internet, not
just this one. Click **More info → Run anyway**.

**Colors look wrong or missing, everything is plain text.**
You're likely on an older Windows version or a terminal that doesn't
support ANSI colors. Try running it from **Windows Terminal** (built into
Windows 11, free from the Microsoft Store on Windows 10) instead of the
old `cmd.exe` window.

**The window closes immediately.**
Don't double-click it from a folder where Explorer closes the window on
exit — instead open a terminal (PowerShell or Windows Terminal), `cd` to
the folder, and run `.\tetris.exe` so the window stays open and you can
see any error message.

## Want to build it yourself instead?

See `CODE_OVERVIEW.md` for how the code is put together, or check the
source in `tetris.cpp` — it's a single file, no external libraries, and
builds with one command (`g++ -std=c++17 -O2 -o tetris.exe tetris.cpp`).
