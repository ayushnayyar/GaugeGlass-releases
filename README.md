# AI Limits — release channel

This repository hosts the public **auto-update feed** and **signed release binaries** for
[AI Limits](https://ailimits.app) — a macOS menu-bar app that shows your Claude Code usage limits
at a glance.

- `appcast.xml` — the [Sparkle](https://sparkle-project.org) update feed the app checks. Served at
  `https://raw.githubusercontent.com/ayushnayyar/AI-Limits-releases/main/appcast.xml`.
- **[Releases](../../releases)** — the notarized `.dmg` for each version.

The application source is not part of this repository. AI Limits is a paid, closed-source app;
this channel exists only so the app can verify and download its own signed updates.

Every update is protected by **two independent signatures** — an EdDSA signature checked against the
public key baked into the app, *and* Apple Developer ID notarization — so a tampered or
man-in-the-middle update is rejected.

---

AI Limits is an independent project, not affiliated with or endorsed by Anthropic.
"Claude" and "Claude Code" are trademarks of Anthropic, PBC.
