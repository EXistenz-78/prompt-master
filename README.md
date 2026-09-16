# Prompt Master 2.0

A free macOS companion app for building prompts for [Draw Things](https://drawthings.ai/), the on-device Stable Diffusion / FLUX / Ideogram app for Apple Silicon.

Prompt Master 2.0 is a structured term database (40 categories, 875 curated terms, fully bilingual IT/EN) paired with a per-model prompt composer. Pick a target model family — Midjourney-style dialects, FLUX.1/2, Krea 2, Qwen-Image, Z-Image, the Stable Diffusion family (1.5 / XL / 3.5), Pony, Illustrious, Ideogram, or Ideogram 4 — and the app adapts vocabulary, prompt syntax, negative-prompt support, and length targets to that model's own conventions, instead of one generic prompt that works so-so everywhere.

Ideogram 4's structured JSON captioning format gets its own dedicated builder: a guided `high_level_description` → `style_description` → `compositional_deconstruction` flow, with database-backed dropdowns for aesthetics, lighting, photo/art style and medium, a visual canvas for placing bounding boxes, and live JSON preview (editable and re-importable).

Optional integrated translation (via your own DeepL API key, kept only in a local proxy on your Mac — never uploaded anywhere) lets you draft in Italian and get a clean English prompt on copy.

## Status

Free public beta. Feedback, bug reports and term suggestions are welcome — open an [Issue](../../issues) here, or find the author on the official Draw Things Discord.

## Requirements

- macOS 11 or later
- Apple Silicon or Intel 64-bit

## Install

1. Download the latest `.zip` from [Releases](../../releases).
2. Unzip it and drag **Prompt Master 2.app** into `/Applications`.
3. See **"First launch"** below before opening it.

## First launch (important)

This build is signed with a free Apple ID, not with a paid Apple Developer ID, and it is **not notarized**. macOS Gatekeeper will refuse to open it the first time — this is expected, not a broken download.

When you see *"Apple could not verify 'Prompt Master 2' is free of malware"*:

1. Open **System Settings → Privacy & Security**.
2. Scroll down — you'll see a line about **"Prompt Master 2" was blocked**.
3. Click **Open Anyway**, then confirm again in the dialog that appears.

You only need to do this once per download.

## License

All rights reserved for now — source is not included in this repository at this stage.
