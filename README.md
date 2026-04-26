## Overview
This project is a C application that visualizes the function y = f(x) using Perlin noise. It includes features like mouse interaction, real-time updates, and cross-platform compilation.

## Features
- Generates Perlin noise to create a dynamic 1D graph.
- Real-time rendering of the graph based on user interactions.
- Cross-platform support including Linux, Windows, Wine, and WebAssembly.

## Project Structure
```
Gui_PerlinNoise_1D/
├── build/              # .exe files produced by Main.c
├── src/
│   ├── Main.c          # Entry point
│   ├── Window.h        # Header file for window management
│   └── PerlinNoise.h   # Header file for Perlin noise generation
├── Makefile.linux      # Linux Build configuration
├── Makefile.windows    # Windows Build configuration
├── Makefile.wine       # Wine Build configuration
└── Makefile.web        # Emscripten Build configuration
```

### Prerequisites
- GCC or Clang C/C++ compiler and debugger
- Make utility
- Standard development tools

## Build & Run
### Linux
1. Clone the repository.
2. Navigate to the project directory.
3. Build the project:
   ```sh
   make -f Makefile.linux all
   ```
4. Run the executable:
   ```sh
   ./build/Main
   ```

### Windows
1. Clone the repository.
2. Navigate to the project directory.
3. Build the project:
   ```sh
   make -f Makefile.windows all
   ```
4. Run the executable:
   ```sh
   build\Main.exe
   ```

### Wine
1. Clone the repository.
2. Navigate to the project directory.
3. Build the project for Windows compatibility:
   ```sh
   make -f Makefile.wine all
   ```
4. Run the executable using Wine:
   ```sh
   WINEPREFIX=~/wine64 WINEARCH=win64 wine build/Main.exe
   ```

### WebAssembly
1. Clone the repository.
2. Navigate to the project directory.
3. Build the project for web browsers:
   ```sh
   make -f Makefile.web all
   ```
4. Open `build/index.html` in a web browser.

These steps will help you build and run the Perlin noise visualization application on different platforms.