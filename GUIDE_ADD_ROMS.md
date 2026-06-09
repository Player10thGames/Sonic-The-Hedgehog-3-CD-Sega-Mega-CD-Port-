# How to Add ROMs for Sonic The Hedgehog 3 (Sega Genesis/MegaDrive)

This guide explains how to add and structure ROM files for Sonic The Hedgehog 3 within this project repository for use with emulators, flash carts, or ROM hacking purposes.

## Understanding Sonic 3 ROMs

Sonic The Hedgehog 3 was originally released as a standard Sega Genesis/MegaDrive cartridge. Later, *Sonic & Knuckles* was released with "Lock-On Technology," allowing players to physically plug the Sonic 3 cartridge into the top of the Sonic & Knuckles cartridge to create the complete game: *Sonic 3 & Knuckles*.

When dealing with ROMs for emulation or hacking, you will typically encounter three distinct files:
1. `Sonic The Hedgehog 3.md` (or `.bin`, `.gen`) - The standalone Sonic 3 game.
2. `Sonic & Knuckles.md` - The standalone S&K game.
3. `Sonic 3 & Knuckles.md` - The combined ROM image.

For Mega-CD porting projects or full disassemblies, the combined *Sonic 3 & Knuckles* ROM is the standard base used by the community [1].

## Repository Structure for ROMs

To keep the repository organized, we have established a specific directory structure for original ROM files. 

*Note: For legal reasons, actual copyrighted ROM files (`.md`, `.bin`, `.gen`) are NOT included in this repository. You must provide your own legally obtained ROM backups.*

Please place your ROM files in the `roms/` directory at the root of the project:

```text
Sonic-The-Hedgehog-3-CD-Sega-Mega-CD-Port-/
├── roms/
│   ├── Sonic 3.md                 <-- Place standalone Sonic 3 ROM here
│   ├── Sonic & Knuckles.md        <-- Place standalone S&K ROM here
│   └── Sonic 3 & Knuckles.md      <-- Place combined S3&K ROM here
├── README.md
└── ...
```

## How to Add Your ROMs

1. **Obtain the ROMs:** Dump your physical Sonic 3 and Sonic & Knuckles cartridges using a dumper like the Retrode, or locate your legally obtained backup files.
2. **Format Verification:** Ensure your ROMs are in standard binary format (usually denoted by `.md` or `.bin` extensions). If they are in `.smd` (interleaved) format, they may need to be converted to standard binary format using a ROM utility tool before they can be used with modern hacking tools or disassemblies.
3. **Copy to Directory:** Copy the files into the `roms/` folder in your local clone of this repository.
4. **Integration with Disassemblies (Advanced):** If you are using a split disassembly (like the Sonic Retro `skdisasm`), the build scripts often require a pristine, byte-perfect original ROM to extract data from during the build process [1]. Ensure the filenames match what your specific build scripts or tools are expecting.

## Using the ROMs

Once added to the `roms/` directory, these files can be:
- Loaded directly into Sega Genesis emulators (like Kega Fusion, BlastEm, or Genesis Plus GX).
- Copied to an SD card for use in an EverDrive or Mega EverDrive flash cartridge.
- Used as base files for ROM hacking tools (like SonLVL, SonED2, or Flex 2).

## References
[1] Sonic Retro. "Sonic and Knuckles Disassembly". https://github.com/sonicretro/skdisasm
