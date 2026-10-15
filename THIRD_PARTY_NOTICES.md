# Third-Party Notices

Universal Couch 64 is built with open-source software and the Discord Social SDK. Those components remain under their own licences, and Universal Couch claims no ownership of them.

**The complete notices** for the app itself, covering every bundled package of v0.6.3 and every licence text, are in **[THIRD_PARTY_NOTICES.txt](THIRD_PARTY_NOTICES.txt)**. That file is identical to the one the v0.6.3 installer places in the install folder.

From v0.6.3 the Universal Couch 64 installer contains **no game-specific runtime**. The GoldenEye XBLA runtime that was installed with v0.6.2-rc.6 now ships with the separate [GoldenEye XBLA Co-op Converter](https://github.com/SzebaHUN/goldeneye-xbla-coop-converter), which publishes its notices and LGPL source offer. The notices for the runtime installed by v0.6.2-rc.6, including that release's LGPL source offer, remain here: **[THIRD_PARTY_NOTICES-goldeneye-runtime.txt](THIRD_PARTY_NOTICES-goldeneye-runtime.txt)**.

## Summary (v0.6.3 installer)

| Component | Licence / terms | Notes |
|---|---|---|
| Tauri, Rust crates and npm packages (React etc.) | MIT, Apache-2.0, BSD, ISC, Zlib and similar | Full list and texts in `THIRD_PARTY_NOTICES.txt` |
| cssparser, cssparser-macros, dtoa-short, option-ext, selectors | MPL-2.0 | Used unmodified. Source is available from crates.io and the upstream repositories (MPL-2.0 §3.2) |
| SDL3 (`SDL3.dll`) | Zlib | Licence text installed as `resources\SDL3-LICENSE.txt` |
| Discord Social SDK (`discord_partner_sdk.dll`) | Discord Developer Terms | © Discord Inc. Its notices are installed as `resources\discord-social-sdk-notices.txt`. Discord and the Discord logo are trademarks of Discord Inc. |

## Not included in the installer

- **Project64** (GPL-2.0) is downloaded by the app from the official Project64 website at the user's request. It is a separate program under its own licence.
- **Microsoft Edge WebView2 Runtime** is installed by Microsoft's own bootstrapper when missing, under Microsoft's licence terms.
- **Game packages and game files.** `.uc64` packages are made on the user's PC from the user's own game files by separate converters (for example the [GoldenEye XBLA Co-op Converter](https://github.com/SzebaHUN/goldeneye-xbla-coop-converter)), which carry their own notices.