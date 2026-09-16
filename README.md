# Prompt Master 2.0

A free macOS companion app for building prompts for [Draw Things](https://drawthings.ai/), the on-device Stable Diffusion / FLUX / Ideogram app for Apple Silicon. This is an independent community project — not affiliated with or endorsed by Draw Things Technologies.

Prompt Master 2.0 was born out of a very concrete problem: if English isn't your first language, writing prompts that actually use the *correct* photography, art-history and technical vocabulary these models were trained on is harder than it looks — and every model family expects that vocabulary phrased its own way. The app pairs a structured, curated term database with a per-model composer, so you pick real terms instead of guessing English words, and the app fine-tunes how they come together for the model you're actually targeting.

Pick a target model family — Midjourney-style dialects, FLUX.1/2, Krea 2, Qwen-Image, Z-Image, the Stable Diffusion family (1.5 / XL / 3.5), Pony, Illustrious, Ideogram, or Ideogram 4 — and the app adapts vocabulary, prompt syntax, negative-prompt support, and length targets to that model's own conventions, instead of one generic prompt that works so-so everywhere.

Ideogram 4's structured JSON captioning format gets its own dedicated builder: a guided `high_level_description` → `style_description` → `compositional_deconstruction` flow, with database-backed dropdowns for aesthetics, lighting, photo/art style and medium, a visual canvas for placing bounding boxes, and live JSON preview (editable and re-importable).

## Languages

The app interface and the term database are both bilingual (Italian / English) for now — the whole app, database terms included, works fine if you only read English. This started as a personal tool built by an Italian speaker, so those are the only two languages it currently supports. Adding more languages is very much on the roadmap, but it's a lot of terminology to translate and curate — and more importantly, it really needs a native speaker for each language to get it right. Help from the community is genuinely what will make that happen. Open an Issue if you'd like to contribute a language.

## Usage notes

A couple of things that aren't obvious from just opening the app:

- **Term database, always in English output.** Whatever language you browse the database in, the terms that actually go into your prompt are the curated English ones — that's the whole point: correct terminology without having to know it yourself.
- **Free-text fields aren't auto-translated by the database** — they're your own words (subject, scene, anything the database doesn't cover). For those, the app can call **DeepL** to translate your Italian draft to English. This needs your own free DeepL API key (deepl.com/pro-api, free tier is enough for personal use), entered once in Preferences — it's used only by a small local proxy that runs on your own Mac, and the key never leaves it.
- **"Briefing for an LLM."** For every model family *except* Ideogram 4, the app doesn't generate the final prose prompt itself — instead it prepares a ready-to-paste **briefing** (a system prompt with that model's own rules, plus your subject and selected terms) that you hand to an LLM of your choice (Claude, ChatGPT, or anything else) to actually draft the final prompt. That result can then be pasted into DrawThings. Ideogram 4 is the one exception: since its output is a structured JSON object, not prose, the app builds it deterministically from your selections — no LLM needed there.

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

This isn't open source (no source is published at this stage) — think of this as freeware terms rather than an OSS license:

- You're welcome to download, install and use the app free of charge, for personal use.
- Please don't redistribute the app yourself, rebrand it, or resell it — link back here instead so people always get the current build and instructions.
- The app is provided as-is, with no warranty of any kind — use it at your own risk.
- All rights are reserved by the author. These terms may evolve as the project does (for instance, a possible future paid tier alongside a free one) — this beta will keep working under the terms it was downloaded with.

This is a plain-language summary, not a lawyer-drafted license — if that ever becomes important (e.g. once monetization is on the table), it's worth having an actual EULA reviewed by a professional at that point.
