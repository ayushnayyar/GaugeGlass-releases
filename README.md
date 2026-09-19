# GaugeGlass — release channel

This repository hosts the public **signed release binaries** for
[GaugeGlass](https://mangostruck.com/gaugeglass) — a macOS menu-bar app that shows your Claude
Code and Codex usage limits at a glance.

- **[Releases](../../releases)** — the notarized `.dmg` for each version. This is what the
  download button on the website points at, and what Sparkle fetches when you install an update.
- `appcast.xml` — a committed copy of the [Sparkle](https://sparkle-project.org) update feed,
  kept here as the canonical build artefact and a fallback. **The app does not read it from
  here**: its feed URL is `https://mangostruck.com/gaugeglass/appcast.xml`.

The application source is not part of this repository, and never will be. GaugeGlass is a paid,
closed-source app; this channel exists only so the app can verify and download its own signed
updates, and so the website has a stable place to link a download.

Every update is protected by **two independent signatures** — an EdDSA signature checked against
the public key baked into the app, *and* Apple Developer ID notarization — so a tampered or
man-in-the-middle update is rejected even though the file is served from a third party.

Downloading a release tells GitHub the usual things any file download does: your IP address, your
user agent, and which version you fetched. GaugeGlass sends no licence key, no account and no
usage data with that request. See the
[privacy policy](https://mangostruck.com/gaugeglass/privacy) for everything the app contacts.

---

GaugeGlass is an independent project, not affiliated with or endorsed by Anthropic or OpenAI.
"Claude" and "Claude Code" are trademarks of Anthropic, PBC. "Codex" is a trademark of OpenAI.
