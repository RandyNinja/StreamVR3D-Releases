# Changelog

## [v0.6.56 preview](https://github.com/RandyNinja/StreamVR3D-Releases/releases/tag/v0.6.56) — 25 September 2026

- Refreshed the cinema interface with selected-title artwork, translucent panels, an icon-rail sidebar, a trailer tile when available, and tinting from the four existing colour themes.
- Home addon catalogue rows load in the background, show status, retry failures, and move repeatedly failing rows below working rows for that session.
- Removed the Back on Screen IMAX row from Home to restore scrolling to the last row on Quest 3. The IMAX catalogue remains in the addon browser.
- Adult addon rows on Home are off by default and can be enabled individually after unlocking Adult VR.
- Added optional experimental trailer autoplay after a four-second non-adult title-card selection. It is off by default; the manual trailer button remains.
- Quest 3 Home scrolling was confirmed on this build. The redesigned interface, background rows, adult Home opt-in, and trailer behavior have not had separate headset interaction checks. Quest 2 remains untested on physical hardware.
- MDBList watchlist screens are included, but pairing requires a registered app ID that is not configured by default in this build. Developer Mode allows manual app ID entry. Live MDBList service testing is not documented.
- Known limitation: seeking an 8192×4096 HEVC 59.94 fps video caused decoder buffer-allocation errors on Quest 3.

Earlier public previews and their notes remain available on the [Releases page](https://github.com/RandyNinja/StreamVR3D-Releases/releases).
