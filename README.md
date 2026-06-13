# OY.Surf

A local-first visual workbench for designers, on your Mac.

**[⬇︎ Download the latest version](../../releases/latest)** · Apple Silicon · free while in beta

---

## Why

Your work lives in a mess of folders. Dropbox, Downloads, render output, a few
hundred AI generations you'll never find again. Finder shows it back to you as a
list of file names. To actually *look* at it — compare two renders, pull a prompt
off a reference, read the text on an image — you end up dragging files through a
dozen apps.

OY.Surf is the one place for that middle of the work: the references, the
versions, the dead ends, the things you're still deciding on. Point it at a
folder and it becomes a gallery you can think in.

## Philosophy

- **Local-first.** Every model runs on your Mac. No account, no telemetry, no
  upload. There is no server that could see your files.
- **No import.** It reads your folders in place and keeps up with changes. No
  second library to maintain, no copies.
- **Your formats stay open.** Notes are plain markdown in your own folders. Your
  files are yours.
- **The tool gets out of the way.** Monochrome interface, content edge to edge,
  built for the keyboard. The work is what you look at.

## What it does today

- **Browse** — open any folder and it turns into a fast masonry gallery of
  images, renders, video, and PDFs.
- **Lenses** — inspect any file the way a designer needs to: pull the color
  palette, write a prompt from an image, read text with OCR, break a video into
  scenes, find similar or duplicate frames, compare a few side by side, or just
  ask about the selection.
- **Create** — generate images on-device from a prompt or a reference. The
  result lands right in your folder, next to everything else.
- **Notes** — Granola-grade markdown notes on any file, with voice dictation
  cleaned up locally and full-text search. Run a slideshow for crit and rate from
  the keyboard.
- **For agents** — a local MCP server, so tools like Claude and Cursor can search
  and organize your library with your approval.

## How it works

- macOS on Apple Silicon. ~200 MB installer, signed with a Developer ID and
  notarized by Apple, with auto-updates built in.
- The app is an Electron + React + TypeScript shell. A local Python sidecar runs
  the machine-learning models.
- The models, all running on your Mac:
  - **Gemma** — vision and text: prompts, tags, descriptions, scene reading.
  - **Whisper** — speech: voice notes, dictation, transcripts.
  - **Z-Image Turbo** — image generation (MLX / Apple Silicon).
  - **Apple Vision** — OCR, built into macOS.
- Models download once on first use; everything after that works offline.
- Cloud models are optional and opt-in (via OpenRouter), never required and never
  the default.

## Where it's going

- **Canvas** — an infinite spatial canvas to lay references and generations out,
  group them, and think across a whole project instead of one folder at a time.
- **AI nodes** — chain the lenses and generation into small node graphs: take a
  palette, feed it a prompt, branch a few variations, compare. Reusable, on-device.
- **Speed** — semantic and visual search with on-device embeddings, faster
  indexing, libraries in the hundreds of thousands.
- **Web + sync** — a web version that syncs with the Mac app, so the same library
  and work follow you off the desktop.

---

This repository hosts the release artifacts and the auto-update manifest
(`latest-mac.yml`). The application source is private.

Made by [Changes Company](https://changes.company).
