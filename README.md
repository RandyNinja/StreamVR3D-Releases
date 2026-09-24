# StreamVR3D

StreamVR3D is a Quest VR cinema app with an optional Windows setup companion. The app is planned as a free binary release. Development source is private.

## What it does

- Plays flat video and stereoscopic side-by-side or top-and-bottom video on a virtual cinema screen.
- Supports immersive VR180 and VR360 equirectangular VR playback.
- Requests HDR-to-SDR tone mapping for HDR sources, including Dolby Vision where the device decoder supports it. The player indicates when conversion is verified and warns when it is not.
- Provides subtitle selection, picture controls, and adjustable screen placement for flat video.
- Browses film and series catalogues through configured add-ons, with watch history and local settings.
- Supports optional adult live streams through user-configured third-party add-ons. This is for adults 18 or older, subject to any higher local legal age. It requires Developer Mode and adult controls; Kids profiles cannot access it. Availability depends on the provider. Profile and PIN controls do not verify age.

## Quest installation requirements

**Quest 3 is the only headset tested so far.** Compatibility with other Quest models is unverified. The current installation path needs a Windows PC, a data-capable USB-C cable, Meta developer access with Developer Mode enabled, USB debugging approval on the headset, and Android Studio with Android SDK Platform-Tools and Build-Tools installed from Google. The Windows companion helps install the Quest app; it is not a PC video player. See the [installation guide](docs/installation.md) for the steps.

**No public build is available yet.** When release checks are complete, the signed Quest APK, Windows setup package, and SHA-256 checksums will appear on this repository's Releases page. Do not install files described as official StreamVR3D releases from other sites.

StreamVR3D includes no films, streams, third-party subscriptions, or permission to view copyrighted media. Use only media and services you are authorized to access. The default addon recommendations are limited to included features, Cinemeta, OpenSubtitles, and WatchHub availability links. Other recommendations require acknowledged Developer Mode; adult recommendations require a separate adult-content acknowledgement.

## Help and reporting

- [Installation guide](docs/installation.md)
- [Troubleshooting](docs/troubleshooting.md)
- [Support and issue reporting](SUPPORT.md)
- [Private security reporting](SECURITY.md)
- [Binary use and redistribution terms](BINARY_TERMS.md)
- [3D film index sources](DATA_ATTRIBUTION.md)
- [Community conduct](CODE_OF_CONDUCT.md)
- [Changelog](CHANGELOG.md)

Issues and feature requests are welcome. Please keep credentials, personal addon links, device identifiers, and private logs out of public reports.

The source code is not in this repository. GitHub's automatically generated source archives contain only these public documents.
