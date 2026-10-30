# Man of Stick

A two-player local stickman fighting game built with C++ and OpenGL (GLUT). Two stickmen battle it out by jumping and shooting fireballs until one runs out of health — then the winner gets a crown.

---

## Gameplay

- **2 players** share the same keyboard
- Each player has **7 HP**
- Shoot fireballs at your opponent to drain their health
- Last one standing wins — their stickman gets a crown and the loser lays alone on the ground, bleeding to death (sad indeed)
---

## Controls

| Action       | Player 1 (WASD) | Player 2 (Arrow Keys) |
|--------------|-----------------|----------------------|
| Move Left    | `A`             | `←`                  |
| Move Right   | `D`             | `→`                  |
| Jump         | `W`             | `↑`                  |
| Shoot        | `S`             | `↓`                  |

> Shooting fires a fireball in the direction the stickman is currently facing.

---

## Requirements

- C++ compiler (g++ with C++11 or later)
- OpenGL
- GLUT (or FreeGLUT)

### Installing dependencies on Ubuntu/Debian

```bash
sudo apt install freeglut3-dev
```

### Installing on macOS (with Homebrew)

```bash
brew install freeglut
```
### Installing on windows

Download from websites

---

## Building & Running
On linux:
```bash
g++ -o stickman stickman.cpp -lGL -lGLU -lglut
./stickman
```

On macOS:
```bash
g++ -o stickman stickman.cpp -framework OpenGL -framework GLUT
./stickman
```
On windows:
```bash
g++ -o stickman.exe stickman.cpp -lfreeglut -lopengl32 -lglu32
./stickman.exe
```
You'll be prompted to enter names for both players in the terminal before the window opens.

---

## Features

- Randomly assigned player colors each game (red, green, blue, magenta, cyan, orange, purple)
- Health bar displayed above each stickman
- Player names rendered above their character
- Fireballs travel across the screen and disappear on hit or leaving the window
- Jump mechanic with auto-gravity (returns to ground after 200ms)
- Winner's stickman displays a crown after the game ends
- Loser screen showing the defeated stickman with a "FATALITY" label
- Draw condition if both players die simultaneously

---

## Notes (not limitations)

- The window size is fixed at **900×900** (why would anyone want a different size?)
- Both players share the same machine — no network play (encouraging in-person communication)
- Player colors are randomized at startup but may occasionally be the same color (can be called destiny?)
