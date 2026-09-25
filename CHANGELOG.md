# Changelog

## [v0.6.56 preview](https://github.com/RandyNinja/StreamVR3D-Releases/releases/tag/v0.6.56) — 25 September 2026

- Removed the Back on Screen IMAX row from Home to restore scrolling to the last row on Quest 3. The IMAX catalogue remains in the addon browser.
- Adult addon rows on Home are off by default and can be enabled individually after unlocking Adult VR.
- Added an optional experimental trailer preview after a four-second title-card selection. It is off by default.
- Quest 3 Home scrolling was confirmed on this build. Adult Home opt-in and trailer behavior passed code tests but have not had separate headset interaction checks. Quest 2 remains untested on physical hardware.
- Known limitation: seeking an 8192×4096 HEVC 59.94 fps video caused decoder buffer-allocation errors on Quest 3.

Earlier public previews and their notes remain available on the [Releases page](https://github.com/RandyNinja/StreamVR3D-Releases/releases).
