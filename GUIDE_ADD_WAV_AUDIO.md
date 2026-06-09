# How to Add Music WAV Audio Files for Sonic The Hedgehog 3 CD (Sega Mega-CD)

This guide details how to add, format, and integrate Red Book audio (CDDA) WAV files into the Sonic The Hedgehog 3 CD Sega Mega-CD port.

## Understanding Mega-CD Audio

Unlike the Sega Genesis/MegaDrive which relies primarily on its internal Yamaha YM2612 FM synthesizer chip for music, the Sega Mega-CD allows for streaming high-quality, uncompressed audio directly from the disc, known as CD-DA (Compact Disc Digital Audio) [1]. 

In a Sega CD game's file structure, Track 1 is the game data, and Tracks 2 and onwards are the audio tracks. When burning or emulating, these audio tracks are often provided as individual `.wav` files referenced by a `.cue` sheet [2].

## Required WAV Format

For the Mega-CD hardware (or emulators) to correctly process and play the audio tracks without speed or pitch issues, your WAV files **must** adhere strictly to the Red Book audio standard [2]:

*   **Format:** Uncompressed PCM WAV
*   **Sample Rate:** 44100 Hz (44.1 kHz)
*   **Bit Depth:** 16-bit
*   **Channels:** Stereo (2 channels)

If you have music in MP3, FLAC, or OGG formats, you must convert them to the above WAV specifications using audio conversion software like Audacity, Switch Sound File Converter, or FFmpeg before adding them to the project.

## Repository Structure for Audio

Place your formatted WAV files into the `audio/wav/` directory.

```text
Sonic-The-Hedgehog-3-CD-Sega-Mega-CD-Port-/
├── audio/
│   └── wav/
│       ├── Track 02 - Title Screen.wav
│       ├── Track 03 - Angel Island Zone Act 1.wav
│       ├── Track 04 - Angel Island Zone Act 2.wav
│       └── ...
├── Sonic The Hedgehog 3 CD (USA).bin
├── Sonic The Hedgehog 3 CD (USA).cue
└── ...
```

## Sonic 3 Audio Track Mapping

To recreate the Sonic 3 experience on the Mega-CD, you need to map the game's original zones to specific track numbers. While custom ports can define their own track mapping in the game code, a standard layout based on the original Sonic 3 soundtrack order is as follows [3]:

| Track | Sonic 3 Song / Zone |
| :--- | :--- |
| Track 02 | Title Screen |
| Track 03 | Angel Island Zone - Act 1 |
| Track 04 | Angel Island Zone - Act 2 |
| Track 05 | Hydrocity Zone - Act 1 |
| Track 06 | Hydrocity Zone - Act 2 |
| Track 07 | Marble Garden Zone - Act 1 |
| Track 08 | Marble Garden Zone - Act 2 |
| Track 09 | Carnival Night Zone - Act 1 |
| Track 10 | Carnival Night Zone - Act 2 |
| Track 11 | Icecap Zone - Act 1 |
| Track 12 | Icecap Zone - Act 2 |
| Track 13 | Launch Base Zone - Act 1 |
| Track 14 | Launch Base Zone - Act 2 |
| Track 15 | Mini-Boss |
| Track 16 | Zone Boss (Dr. Robotnik) |
| Track 17 | Final Boss |
| Track 18 | Special Stage |
| Track 19 | Bonus Stage (Gumball Machine) |
| Track 20 | Invincibility |
| Track 21 | Knuckles' Theme |
| Track 22 | Credits |

*Note: Short jingles (like 1-Up, Chaos Emerald, Act Clear) are typically handled by the internal FM synth or PCM chip rather than CDDA, as CD seeking takes too long for instant sound effects.*

## Updating the CUE Sheet

Once your WAV files are in place, you must update the `.cue` file to tell the emulator or CD burning software where the audio tracks are.

Open your `.cue` file in a text editor and append the audio tracks after the main data track. It should look like this:

```text
FILE "Sonic The Hedgehog 3 CD (USA).bin" BINARY
  TRACK 01 MODE1/2352
    INDEX 01 00:00:00
FILE "audio/wav/Track 02 - Title Screen.wav" WAVE
  TRACK 02 AUDIO
    INDEX 01 00:00:00
FILE "audio/wav/Track 03 - Angel Island Zone Act 1.wav" WAVE
  TRACK 03 AUDIO
    INDEX 01 00:00:00
... (continue for all tracks)
```

**Important:** Ensure the paths in the `FILE` commands exactly match the location and names of your WAV files relative to the `.cue` file.

## References
[1] Sudden-Desu. "Quick Intro to Mega CD Development". https://sudden-desu.net/entry/quick-intro-to-mega-cd-development-the-sonic-cd-mmd-loader/
[2] Racketboy Forums. "Burning Mega CD Roms". https://racketboy.com/forum/viewtopic.php?t=12863
[3] Sonic Sound Test Wiki. "Sonic The Hedgehog 3 Soundtrack". https://sonicsoundtest.fandom.com/wiki/Sonic_The_Hedgehog_3_Soundtrack
