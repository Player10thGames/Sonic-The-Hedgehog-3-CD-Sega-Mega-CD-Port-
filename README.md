# Sonic The Hedgehog 3 CD — Sega Mega-CD Port

A ROM hacking and porting project that brings **Sonic The Hedgehog 3** from the Sega Genesis/MegaDrive to the **Sega Mega-CD** platform, taking advantage of the Mega-CD's CD-DA audio streaming capabilities to deliver a fully enhanced audio experience.

---

## What's Included

This repository contains the following files for the Sega Mega-CD port:

| File | Description |
| :--- | :--- |
| `Sonic The Hedgehog 3 CD (USA).bin` | The Mega-CD disc image binary (data + audio) |
| `Sonic The Hedgehog 3 CD (USA).cue` | The CUE sheet for burning or loading in emulators |

---

## Guides

The following guides are provided to help you set up, burn, and extend this project:

| Guide | Description |
| :--- | :--- |
| [GUIDE_BURN_BINCUE.md](GUIDE_BURN_BINCUE.md) | How to burn the Bin/Cue to a CD-R for real hardware |
| [GUIDE_ADD_ROMS.md](GUIDE_ADD_ROMS.md) | How to add Sega Genesis/MegaDrive ROM files to the project |
| [GUIDE_ADD_WAV_AUDIO.md](GUIDE_ADD_WAV_AUDIO.md) | How to add and configure Music WAV Audio Files for the Mega-CD |

---

## Repository Structure

```text
Sonic-The-Hedgehog-3-CD-Sega-Mega-CD-Port-/
├── audio/
│   └── wav/
│       ├── README.md              (WAV file naming conventions and format specs)
│       └── Track XX - Name.wav   (Place your WAV audio files here)
├── roms/
│   ├── README.md                  (ROM file instructions and legal notice)
│   └── Sonic 3.md                 (Place your ROM backups here)
├── Sonic The Hedgehog 3 CD (USA).bin
├── Sonic The Hedgehog 3 CD (USA).cue
├── GUIDE_BURN_BINCUE.md
├── GUIDE_ADD_ROMS.md
├── GUIDE_ADD_WAV_AUDIO.md
└── README.md
```

---

## Quick Start

1. **To play on a real Sega Mega-CD:** Follow the [Bin/Cue Burning Guide](GUIDE_BURN_BINCUE.md) to burn the included `.cue` file to a blank CD-R.
2. **To play in an emulator:** Load the `Sonic The Hedgehog 3 CD (USA).cue` file directly in a Mega-CD compatible emulator such as **Kega Fusion**, **BlastEm**, or **Genesis Plus GX** (RetroArch).
3. **To add music:** Follow the [WAV Audio Guide](GUIDE_ADD_WAV_AUDIO.md) to add Red Book audio tracks and update the `.cue` sheet.
4. **For ROM hacking:** Follow the [ROM Guide](GUIDE_ADD_ROMS.md) to add your Genesis/MegaDrive ROM backups to the `roms/` directory.

---

## Legal Notice

This project is a fan-made ROM hack created for educational and preservation purposes. Sonic The Hedgehog is a trademark of Sega. Copyrighted ROM files and commercial audio assets are not included in this repository. You must provide your own legally obtained backups.

---

*Maintained by Player10thGames*
