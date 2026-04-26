# Project README

## Overview
The project is a C program that generates mazes using the SDL library for graphical output. The main features include:

- Maze generation and rendering.
- Cross-platform support via multiple makefiles.

## Features
- Generates and displays mazes in a window.
- Supports Linux, Windows, Wine, and WebAssembly build environments.

## Project Structure
The project is organized as follows:
```
Gui_Mazes/
├── build/              # .exe files produced by Main.c
├── src/                # Source code
│   ├── Main.c          # Entry point
│   └── *.h             # Standalone Header-based C-files, without *.c files that implement it
├── Makefile.linux      # Linux Build configuration
├── Makefile.windows    # Windows Build configuration
├── Makefile.wine       # Wine Build configuration
├── Makefile.web        # Emscripten Build configuration
└── README.md           # This file
└── LICENSE
└── .gitignore
```

### Prerequisites
- C/C++ Compiler and Debugger (GCC, Clang)
- Make utility
- Standard development tools
- SDL2 library for graphical output

## Build & Run
### Linux
1. Navigate to the project directory:
    ```sh
    cd Gui_Mazes
    ```
2. Build the project:
    ```sh
    make -f Makefile.linux all
    ```
3. Execute the program:
    ```sh
    make -f Makefile.linux exe
    ```

### Windows
1. Navigate to the project directory:
    ```sh
    cd Gui_Mazes
    ```
2. Build the project:
    ```sh
    make -f Makefile.windows all
    ```
3. Execute the program:
    ```sh
    make -f Makefile.windows exe
    ```

### Wine
1. Navigate to the project directory:
    ```sh
    cd Gui_Mazes
    ```
2. Build the project for Wine:
    ```sh
    make -f Makefile.wine all
    ```
3. Execute the program in Wine:
    ```sh
    WINEPREFIX=~/wine64 WINEARCH=win64 wine build/Main.exe
    ```

### WebAssembly
1. Navigate to the project directory:
    ```sh
    cd Gui_Mazes
    ```
2. Build the project for WebAssembly:
    ```sh
    make -f Makefile.web all
    ```
3. Run the WebAssembly application in a web browser:
    ```sh
    emrun --no_browser --port 8080 build/index.html
    ```

These steps provide a comprehensive guide to building and running the project on different platforms.