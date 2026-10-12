# Third-Party Notices

Universal Couch 64 is built with open-source software and the Discord Social SDK. Those components remain under their own licences, and Universal Couch claims no ownership of them.

**The complete notices** for the app itself, covering all 410 bundled packages of 0.6.2-rc.6 and every licence text, are in **[THIRD_PARTY_NOTICES.txt](THIRD_PARTY_NOTICES.txt)**. That file is identical to the one the 0.6.2-rc.6 installer places in the install folder.

The **GoldenEye XBLA runtime** installed with 0.6.2-rc.6 has its own notices: **[THIRD_PARTY_NOTICES-goldeneye-runtime.txt](THIRD_PARTY_NOTICES-goldeneye-runtime.txt)**. It reproduces the runtime's installed `NOTICES.txt` and adds an addendum with components that file does not list, plus the LGPL source offer.

## Summary

| Component | Licence / terms | Notes |
|---|---|---|
| Tauri, Rust crates and npm packages (React etc.) | MIT, Apache-2.0, BSD, ISC, Zlib and similar | Full list and texts in `THIRD_PARTY_NOTICES.txt` |
| cssparser, cssparser-macros, dtoa-short, option-ext, selectors | MPL-2.0 | Used unmodified. Source is available from crates.io and the upstream repositories (MPL-2.0 §3.2) |
| SDL3 (`SDL3.dll`) | Zlib | Licence text installed as `resources\SDL3-LICENSE.txt` |
| Discord Social SDK (`discord_partner_sdk.dll`) | Discord Developer Terms | © Discord Inc. Its notices are installed as `resources\discord-social-sdk-notices.txt`. Discord and the Discord logo are trademarks of Discord Inc. |
| GoldenEye XBLA runtime (`resources\goldeneye-runtime`) | Various open-source licences | rexglue (BSD-3-Clause, incl. portions of Xenia), FFmpeg libavcodec/libavutil and libmspack (LGPL-2.1, statically linked, unmodified; source offer in the runtime notices), Tracy, SDL3, imgui, fmt, spdlog and others. Contains no game data. |
| Microsoft Visual C++ runtime DLLs (in the GoldenEye runtime folder) | Microsoft Visual Studio redistributable terms | Redistributed unmodified |

## Not included in the installer

- **Project64** (GPL-2.0) is downloaded by the app from the official Project64 website at the user's request. It is a separate program under its own licence.
- **Microsoft Edge WebView2 Runtime** is installed by Microsoft's own bootstrapper when missing, under Microsoft's licence terms.
- **Game files.** GoldenEye XBLA game files come only from the user's own copy, packaged on their PC with the separate [GoldenEye XBLA Co-op Converter](https://github.com/SzebaHUN/goldeneye-xbla-coop-converter).
