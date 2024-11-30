# O3-OSD-recording
Mod for recording the O3 osd to file on the DJI goggles V2

## NOTES
- This is a work in progress
- The mod creates a .osd file on the goggles V2 SD card when flying with the O3 Air Unit.
  It works similarly to the OSD recording mod on the Vista or original Air Unit. However, currently, the files created with this mod are incompatible with the online overlay tool. If you want a working solution to create and overlay you can use this python tool: https://github.com/xNuclearSquirrel/O3_OverlayTool
- The .osd file is recorded using the timestamp of the internal clock of the goggles! So it is best overlayed over Air Unit footage, since the goggle side DVR has missing frames which can create a mismatch over time.

##### Install
- coming soon

##### Manual install
- `adb push ipk/O3-OSD-recording_1.0.0_pigeon-glasses-v2.ipk.ipk /tmp`
- open up shell with `adb shell`
- `opkg install /tmp/O3-OSD-recording_1.0.0_pigeon-glasses-v2.ipk`
- or `opkg upgrade /tmp/O3-OSD-recording_1.0.0_pigeon-glasses-v2.ipk` if the version is newer

##### Known issues
- Since the OSD frames are stored with a time stamp, it syncs quite well with the action footage even over long recordings, but it needs to be aligned manually in the video editor. Also I've noticed over very long periods (40 minuts+) the sync can be a few hundred ms off.

##### Credits
- Thanks to Joonas and SNEAKY_FPV for the help when developing this!
