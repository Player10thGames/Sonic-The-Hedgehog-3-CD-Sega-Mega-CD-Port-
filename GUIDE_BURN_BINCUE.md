# How to Burn a Bin/Cue for Sonic The Hedgehog 3 CD (Sega Mega-CD)

This guide provides step-by-step instructions on how to properly burn a `.bin` and `.cue` file set for the Sonic The Hedgehog 3 CD Sega Mega-CD Port to a physical CD-R so it can be played on real hardware.

## Prerequisites

To successfully burn a Sega Mega-CD game, you will need the following:
1. **A blank CD-R**: Do not use CD-RWs, as most original Sega Mega-CD/Sega CD consoles cannot read them reliably. High-quality CD-Rs (like Taiyo Yuden or Verbatim) are recommended.
2. **A CD/DVD Burner drive**: Either internal or external USB.
3. **Burning Software**: **ImgBurn** is highly recommended for Windows users as it properly handles `.cue` sheets and mixed-mode CDs (Data + Audio tracks). For macOS, tools like **Burn** or **LiquidCD** can be used.
4. **The Game Files**: You need both the `.bin` file (containing the game data and audio) and the `.cue` file (the index that tells the burner how to lay out the tracks).

## Understanding the Bin/Cue Format

Sega CD games use a "Mixed Mode" format. Track 1 is typically the game data (MODE1/2352), and the subsequent tracks are standard CD Audio (CDDA) tracks that play the game's background music [1]. 

The `.cue` file is a plain text file that maps out these tracks. It is critical that you **always open and burn the `.cue` file, never the `.bin` or `.iso` file directly**. If you burn just the data file, the game will boot, but you will have no background music [2].

## Step-by-Step Burning Instructions (using ImgBurn)

1. **Download and Install ImgBurn**
   - Download ImgBurn from its official website and install it. (Be careful during installation to decline any bundled adware).

2. **Prepare your Files**
   - Ensure that your `.bin` and `.cue` files are in the same folder.
   - For this project, the files are named `Sonic The Hedgehog 3 CD (USA).bin` and `Sonic The Hedgehog 3 CD (USA).cue`.
   - *Optional Check:* You can open the `.cue` file in a text editor (like Notepad) to verify that the filename referenced inside exactly matches the name of your `.bin` file.

3. **Open ImgBurn**
   - Launch the ImgBurn application.
   - From the main menu, select **"Write image file to disc"**.

4. **Select the Source File**
   - Under the "Source" section, click the "Browse for a file" icon (it looks like a folder with a magnifying glass).
   - Navigate to the folder containing your game files and select the **`Sonic The Hedgehog 3 CD (USA).cue`** file. 

5. **Configure Burn Settings**
   - Insert your blank CD-R into your disc drive.
   - **Write Speed:** It is highly recommended to set the write speed to the lowest possible setting supported by your drive and media (e.g., 4x, 8x, or 16x). Burning at maximum speed can cause read errors on the 30-year-old lasers found in Sega CD hardware [3].
   - Ensure the "Verify" box is checked. This will make ImgBurn check the disc against the original file after burning to ensure there were no errors.

6. **Burn the Disc**
   - Click the large "Write" button at the bottom of the window (the icon showing a file pointing to a disc).
   - Wait for the burning and verification processes to complete. 

7. **Play the Game**
   - Once finished, eject the disc, place it into your Sega Mega-CD / Sega CD console, and power it on!

## Troubleshooting

- **Game boots but has no music:** You likely burned the `.bin` or `.iso` directly instead of the `.cue` file. Re-burn using the `.cue` file.
- **Console doesn't recognize the disc:** Ensure your console's region matches the region of the ROM (USA, EUR, or JAP). If they don't match, you will need to patch the region of the image before burning using a tool like Sega Cue Maker or Sega Region Patcher [2]. Also, verify you used a CD-R and not a CD-RW.

## References
[1] Mega-CD Disc Format Specification. Sega.
[2] Racketboy Forums. "Burning Mega CD Roms". https://racketboy.com/forum/viewtopic.php?t=12863
[3] Retro Game Talk. "Disc Juggler/IMGburn settings to properly burn Sega CD games".
