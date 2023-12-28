# ROM Hack Release Builder

This system automates the process of building a ROM hack release that uses xdelta patches. Creating a patch for multiple regional ROM versions manually can be time-consuming and prone to error, and automating this task can save time and allow releasing updates more frequently. The system can also verify that the base ROMs of each region have the right checksums, and it makes sure that the generated patches all produce the same ROM.

## Instructions
1. Copy the ROM you want to release to the root of this repo. Alternatively, you can also copy the files from this repo to your own project folder.
2. Copy at least one version of the ROM your hack is based on to [clean_roms](clean_roms). You may include base ROMs for multiple regions.
3. Change the settings in [release_settings.json](release_settings.json) as you see fit. The example project is a SM64DS mod, so you'll have to change the `rom_versions` array if your hack is for a different game.
4. Install Python 3 if you haven't already.
5. Run [build_release.py](build_release.py) in cmd.
6. If the script finished after saying "Release created successfully", check the zip file that was created in the `release` folder and upload it somewhere.

xdelta downloaded from https://www.romhacking.net/utilities/598/
