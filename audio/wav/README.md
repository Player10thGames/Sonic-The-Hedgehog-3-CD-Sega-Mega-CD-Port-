# Audio WAV Files Directory

This directory is the designated location for the Red Book CDDA audio tracks used in the Sega Mega-CD version of Sonic The Hedgehog 3 CD.

## Required WAV Format

All WAV files placed here **must** meet the following Red Book audio standard specifications:

| Property | Required Value |
| :--- | :--- |
| Format | Uncompressed PCM WAV |
| Sample Rate | 44100 Hz (44.1 kHz) |
| Bit Depth | 16-bit |
| Channels | Stereo (2 channels) |

## Track Naming Convention

Name your WAV files to match the track numbers referenced in the `.cue` file. The recommended naming format is:

```
Track 02 - Title Screen.wav
Track 03 - Angel Island Zone Act 1.wav
Track 04 - Angel Island Zone Act 2.wav
Track 05 - Hydrocity Zone Act 1.wav
Track 06 - Hydrocity Zone Act 2.wav
Track 07 - Marble Garden Zone Act 1.wav
Track 08 - Marble Garden Zone Act 2.wav
Track 09 - Carnival Night Zone Act 1.wav
Track 10 - Carnival Night Zone Act 2.wav
Track 11 - Icecap Zone Act 1.wav
Track 12 - Icecap Zone Act 2.wav
Track 13 - Launch Base Zone Act 1.wav
Track 14 - Launch Base Zone Act 2.wav
Track 15 - Mini-Boss.wav
Track 16 - Zone Boss.wav
Track 17 - Final Boss.wav
Track 18 - Special Stage.wav
Track 19 - Bonus Stage.wav
Track 20 - Invincibility.wav
Track 21 - Knuckles Theme.wav
Track 22 - Credits.wav
```

## Usage

See [GUIDE_ADD_WAV_AUDIO.md](../../GUIDE_ADD_WAV_AUDIO.md) for full instructions on how to convert, add, and integrate these audio files into the project's `.cue` sheet.
