# Third-Party Notices

Universal Couch 64 is built with open-source software and the Discord Social SDK. Those components remain under their own licences, and Universal Couch claims no ownership of them.

**The complete notices**, covering all 415 bundled packages and every licence text, are in **[THIRD_PARTY_NOTICES.txt](THIRD_PARTY_NOTICES.txt)**. That file is identical to the one the installer places in the install folder.

## Summary

| Component | Licence / terms | Notes |
|---|---|---|
| Tauri, Rust crates and npm packages (React etc.) | MIT, Apache-2.0, BSD, ISC, Zlib and similar | Full list and texts in `THIRD_PARTY_NOTICES.txt` |
| cssparser, cssparser-macros, dtoa-short, option-ext, selectors | MPL-2.0 | Used unmodified. Source is available from crates.io and the upstream repositories (MPL-2.0 §3.2) |
| SDL3 (`SDL3.dll`) | Zlib | Licence text installed as `resources\SDL3-LICENSE.txt` |
| Discord Social SDK (`discord_partner_sdk.dll`) | Discord Developer Terms | © Discord Inc. Its notices are installed as `resources\discord-social-sdk-notices.txt`. Discord and the Discord logo are trademarks of Discord Inc. |

## Not included in the installer

- **Project64** (GPL-2.0) is downloaded by the app from the official Project64 website at the user's request. It is a separate program under its own licence.
- **Microsoft Edge WebView2 Runtime** is installed by Microsoft's own bootstrapper when missing, under Microsoft's licence terms.
