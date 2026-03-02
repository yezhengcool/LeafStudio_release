# EmulatorJS Data Files (OFFLINE READY)

This directory contains the fully integrated EmulatorJS engine with local core files.

## Directory Structure
- `data/loader.js`: The main loader script.
- `data/emulator.min.js`: The emulator engine.
- `data/cores/`: Contains the original libretro core files (`.js` and `.wasm`).

## Installed Cores (Original Names for WASM Compatibility)
The following cores are correctly installed in `data/cores/`:

- **NES**: `nestopia_libretro.js`
- **SNES**: `snes9x_libretro.js`
- **GB/GBC**: `gambatte_libretro.js`
- **GBA**: `mgba_libretro.js`
- **Sega Genesis/MD**: `genesis_plus_gx_libretro.js`
- **PlayStation 1 (PSX)**: `pcsx_rearmed_libretro.js`
- **Nintendo 64 (N64)**: `mupen64plus_next_libretro.js`
- **Nintendo DS**: `melonds_libretro.js`
- **Arcade (MAME)**: `mame2003_plus_libretro.js`
- **Arcade (FBNeo)**: `fbneo_libretro.js`

## Why Original Names?
The compiled JS for each core has the WASM filename hardcoded inside it (e.g., `nestopia_libretro.wasm`). Renaming the `.js` file to `nes.js` without updating the internal string causes the WASM load to fail, resulting in a black screen. We keep the original names to ensure 100% compatibility.
