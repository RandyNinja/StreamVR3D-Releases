# Changelog


## [v0.6.108 preview](https://github.com/RandyNinja/StreamVR3D-Releases/releases/tag/v0.6.108) — 30 September 2026

- Restored Sources and catalogue thumbstick scrolling by routing shelf input only from the controller whose pointer is over the shelf. Invalid controller ownership no longer falls back to the left-hand ray.
- Screen grip starts only after a direct ray hit on the movie screen. The flat cinema can reach 800% size and 30 m distance, with faster grip controls, larger steps, expanded offsets, and size presets through 800%. Curvature is limited when a huge screen is close to the viewer.
- The signed v0.6.108/code 161 APK passed Android IL2CPP build and v3 signature checks. It installed over the prior build on Quest 3 with data preserved and launched without an immediate runtime exception. The owner confirmed the scrolling and cinema controls work. Physical Quest 2 support remains untested; no Windows installer was verified for this build.
- The [v0.6.108 release notes](https://github.com/RandyNinja/StreamVR3D-Releases/releases/tag/v0.6.108) now include a full improvement summary since v0.6.89: redesigned tinted-glass menus, compact playback rail and separate controls panel, trailer autoplay, My List shelf, clearer rendering, high-precision video bridge, Reset View and grip placement, and navigation fixes.

## [v0.6.106 preview](https://github.com/RandyNinja/StreamVR3D-Releases/releases/tag/v0.6.106) — 29 September 2026

- Controller B/Y and Escape Back now take priority over optional refresh work and remain responsive while busy. Independent controller presses are handled separately.
- Fixed Back behavior in the playback rail, source filters, and season picker. Stale focus overlays no longer intercept Back; pending source, autoplay, and cloud callbacks are invalidated when leaving their screens.
- The signed v0.6.106/code 159 Quest APK passed Android v3 signature verification and 626 Unity EditMode tests. It installed as an update on Quest 3 with app data preserved, and the owner confirmed the controller Back fix. Wider headset interactions and physical Quest 2 support remain unverified. No Windows installer was verified for this build.

## [v0.6.89 preview](https://github.com/RandyNinja/StreamVR3D-Releases/releases/tag/v0.6.89) — 26 September 2026

- Started Live TV integration for channels supplied by compatible installed addons. The Live TV page offers country/category filters, selected-channel preview, and optional programme guides; no channels are bundled. Earlier Quest testing confirmed one MediaFusion channel, but broad addon and guide compatibility remains unverified.
- Anime now separates TV series and Movies catalogues and offers an optional English-dub catalogue filter for the included Anime Catalogs source. The filter affects catalogue entries, not playback audio tracks.
- Improved addon catalogue navigation, TMDB Collections browsing, duplicate-addon setup choices, and playback seeking/recovery. Added Clear links to the in-headset addon setup browser; its interactive Quest check remains pending.
- The signed v0.6.89/code 142 Quest APK passed Android v3 signature and 16 KB alignment checks, and 561 Unity EditMode tests passed. It installed as an update on Quest 3. Replaying the previously crash-causing Dolby Vision Profile 7 source showed an unsupported warning without an app crash; Profile 7 remains unplayable. Physical Quest 2 support and broader headset checks remain pending. No Windows installer was verified against this APK.



## [v0.6.69 preview](https://github.com/RandyNinja/StreamVR3D-Releases/releases/tag/v0.6.69) — 26 September 2026

- Movies, TV, Anime, and compatible addon catalogues use a unified five-column grid. Adult VR retains six columns with row-by-row navigation. Returning from details restores focus and position.
- Compatible addon catalogues can appear in the matching menus. Provider and genre pages load independently, continue after short pages, and retry failures. Recent sorting uses full provider dates when available.
- Enlarged the Home hero and trailer area, reduced repeated catalogue reads and artwork cache evictions, and fixed clipping in Settings and source summaries.
- Published the signed v0.6.69/code 122 Quest APK with a matching SHA-256 file. The Android v3 signature and 16 KB alignment were verified; 490 Unity EditMode tests and 35 offline interface fixture checks passed. It installed as an update on Quest 3 and Android reported v0.6.69/code 122.
- Interactive headset testing, live configured addons, native playback, headset performance, and Quest 2 remain unverified for this build. The Real-Debrid red-link/Access Denied issue is paused and is not fixed here. No Windows installer was verified against this APK.

## [v0.6.61 preview](https://github.com/RandyNinja/StreamVR3D-Releases/releases/tag/v0.6.61) — 25 September 2026

- Passed safe, non-credential Stremio request headers into Media3 playback; credential headers remain excluded.
- Separated resolved HTTPS addon playback from Premiumize cloud transfer. Unresolved magnets need a playable link; only explicitly Premiumize-identified sources can trigger the app's Premiumize cache check.
- Improved the standalone Real-Debrid provider's single-video selection and error messages. It is not wired to the Quest cloud UI; there is no native Real-Debrid account integration.
- Published matching v0.6.61/code 114 Quest APK and Windows installer bundle. The installer ZIP contains the same signed APK.
- 440 Unity EditMode tests, 34 installer checks, and Android v3 signature verification passed. This build has not had a Quest install or visual check. Real-Debrid behavior was tested with simulated responses; Quest 2 remains untested on physical hardware.



## [v0.6.59 preview](https://github.com/RandyNinja/StreamVR3D-Releases/releases/tag/v0.6.59) — 25 September 2026

- Source cards distinguish Premiumize-verified cache status from addon-reported cache claims; magnet links no longer show a misleading blue CACHE action.
- Without Premiumize connected, playable HTTPS links resolved by configured addons can appear in Sources. Magnet-only rows and Premiumize cloud transfer are omitted. An addon still has to supply a playable link.
- Premiumize cloud transfers show clearer submission progress and errors.
- APK v0.6.59/code 112 passed 435 Unity EditMode tests, Android v3 signature verification, and a Quest 3 install and launch over the v0.6.58 candidate. Real-Debrid-only playback on the affected headset and Quest 2 hardware support remain unverified.
- APK-only release; no v0.6.59 Windows installer was built.


## [v0.6.57 preview](https://github.com/RandyNinja/StreamVR3D-Releases/releases/tag/v0.6.57) — 25 September 2026

- Shortened optional experimental trailer autoplay from four seconds to two seconds after explicit selection of a non-adult title card. It remains off by default, and the manual trailer button remains.
- Installed the signed v0.6.57/code 110 APK over v0.6.56 on Quest 3. The two-second trailer interaction has not had a separate headset check. Physical Quest 2 testing remains pending.
- The cinema interface, background Home row loading, BoS IMAX Home fix, and adult Home opt-in continue from v0.6.56.

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
