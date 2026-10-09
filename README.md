# Odesli Gap

A minimal iOS **share extension** that converts any song link (Spotify, Apple Music, etc.) into a universal [song.link](https://song.link) link — so musicians and DJs can share a link that opens the right service for whoever receives it.

**Status: pre-code.** This repo currently holds the build spec only. No source code yet.

## The problem ("the gap")

When a DJ or musician drops a song link into a group chat, the recipient's streaming app may not even have the song — or the link opens a service they don't use. The universal `song.link` solves discovery but forces an awkward two-step copy/paste dance: resolve the link in one app, then paste it into the messenger.

**Odesli Gap closes that.** You share a song once → pick our row in the system share sheet → we resolve it to a `song.link` → the native share sheet hands it straight to WhatsApp / any messenger. Zero friction, feels like normal sharing.

## Product shape

- **Sender side:** native iOS share extension (no App Store, no paid developer account — sideloaded on your own iPhone).
- **Recipient side:** routed via the web (recipient sees the right streaming link automatically).

## Contents

- `build-spec.html` — Part 0 build specification: the full handoff artifact a coding agent builds the MVP from (scope, side-load steps, the share-extension → `UIActivityViewController` flow, and the known catches).
- `README.md` — you are here.

## Build status

The spec is under active adversarial review (kept honest by external review passes; the core mechanism is `UIActivityViewController` presented by the extension itself — no host-app hop, no copy/paste). Code lands next once the spec clears review.
