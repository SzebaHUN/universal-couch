# Privacy Policy

*Version 3 · effective 4 October 2026 · Universal Couch 64 v0.5.8. This is the same text shown inside the app (Support → Terms of Use / Privacy Policy). If the two ever differ, the version shown in the app you installed applies.*

UC64 has no user accounts, no analytics and no advertising. To find friends and connect, some information has to travel over the internet. This page explains what goes where.

## Stays on your PC

- Your ROMs and game files, save files and save states, Project64 and its settings, controller mappings, and UC64's settings (including your nickname and the date you accepted these terms).
- ROM contents, file names, hashes and local file paths are not sent to the relay, the directory or Discord.

## When you play with friends (the people in your room)

- **Game video, audio and controller input** go directly between the host's PC and the players' PCs, encrypted by WebRTC. To set up that direct connection the PCs exchange network addresses (including IP addresses) with each other.
- Everyone in a room sees the other players' nicknames and the name of the game being played. The host's PC tells joined players the game name over that direct, encrypted connection.
- A public STUN server (Google's by default) sees your IP address while helping to find the route between PCs.

## Connection setup relay (Cloudflare)

- Room setup messages (joining, nicknames, session tokens and the connection details mentioned above) pass through UC64's own relay service on Cloudflare Workers. It forwards them live and stores nothing. (Versions before 0.5.0 used the public ntfy.sh relay instead.)
- Since version 0.4.6 these messages are **end-to-end encrypted** (XChaCha20-Poly1305) with a key derived from the room code and password (or the room's random invite secret) using Argon2id. The relay sees only a mailbox name derived the same way, message sizes and timing, an encrypted blob, and your IP address as a normal internet service does. The game name is never sent through the relay. The password itself is never sent.
- The protection depends on the room secret: room codes are random (about 59 bits). Adding a room password makes guessing harder still.

## Public directory (Cloudflare)

UC64's public directory runs on Cloudflare Workers. It receives:

- if you turn on **Discoverable**: your nickname and a generic status such as “Available” or “Hosting · 2/4”, plus whether you linked Discord (and your Discord user id, kept hidden, used only if another linked player asks to add you as a friend);
- if you host a **Public** room: the room's seat count, room code and a random invite secret created for that room, so it can be handed to someone who joins from the public list. Your own room password is never sent;
- if you host while Discord is connected: the room's seat count and, for Discord invites, an encrypted blob the directory cannot read (the key is only inside the Discord invitation).

It never receives game names, ROM information or file paths. Entries disappear about 45 seconds after UC64 stops updating them, or immediately when you close the room or turn Discoverable off; invitation records end with their room (at most 12 hours). Your IP address is used briefly in memory for rate limiting, and Cloudflare also processes requests under its own policies. Private rooms are never listed.

## Discord (optional)

- If you connect Discord, sign-in happens on Discord's own page. Your Discord login is kept by Windows Credential Manager on your PC, not by UC64's services.
- UC64 shows your Discord friends inside the app and sets your Discord activity to “Universal Couch 64” with a generic status (for example “Hosting a room · On the couch”, with seat counts). It never sends the game name to Discord.
- Discord may separately show programs it detects running on your PC (such as Project64); that is Discord's own feature and its settings.
- Invitations you send and accept go through Discord. Discord's privacy policy applies to Discord.

## Downloads

When you set up Project64, UC64 downloads it from the official Project64 website.

## Your choices

- Discoverable is off by default. Rooms are private unless you make them public. Discord is optional and can be disconnected at any time.
- Room codes always work without the directory or Discord.
- Uninstalling UC64 removes the app; your settings and saves stay in your Windows profile folders until you delete them.

## Children

UC64 is not directed at children under 13, and it does not knowingly collect information about them.

## Changes and contact

If this policy changes significantly, UC64 will ask you to review it again. Questions: the project's support page on GitHub (Support → GitHub, or [GitHub Issues](https://github.com/SzebaHUN/universal-couch/issues)).

---

## Additional notes (this website)

- **Log file.** Universal Couch writes a diagnostics log on your PC at `%LOCALAPPDATA%\UniversalCouch\Logs\uc64.log`, which includes connection and media statistics. It is never uploaded automatically. It only leaves your PC if you choose to share it, for example in a bug report.
- **Uninstalling.** If you tick *Delete the application data* in the uninstaller, it also removes the data Universal Couch created on your PC, and asks whether you want to keep your game saves.
- **No crash reporting or telemetry.** Universal Couch does not send crash reports, usage statistics or analytics anywhere.
- **This GitHub page** is hosted by GitHub, and GitHub's privacy policy applies when you visit it. If you use Discord, Discord's own privacy policy applies.
