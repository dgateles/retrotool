<div align="center">

# Retro Tool

**All-in-one management suite for retro gaming collections**

![Version](https://img.shields.io/badge/version-1.0.14-blue.svg)
![Platforms](https://img.shields.io/badge/platforms-Windows%20%7C%20macOS%20%7C%20Linux-8b5cf6.svg)
![Tauri](https://img.shields.io/badge/built%20with-Tauri%202-24c8db.svg)

Scrape metadata, organize media and build gamelists for your ROM library,
powered by [ScreenScraper.fr](https://www.screenscraper.fr).

[Download](https://github.com/dgateles/retrotool/releases/latest) •
[Report a bug](https://github.com/dgateles/retrotool/issues)

</div>

---

## Features

### 🎮 Gamelist Scraper
- **ScreenScraper integration** with accurate game identification by CRC32/MD5 hash, with filename fallback search.
- **Multi-system scraping**: select your ROMs root folder and every recognized console folder is processed in sequence, with a single linear progress bar across all systems.
- **Region-aware media**: box art, thumbnails and videos matching your ROM's region tag (No-Intro naming supported, including multi-region tags like `(USA, Europe)`).
- **Selective scraping**: pick exactly which games to (re)scrape, preserving the rest of your gamelist.
- **Resume support**: interrupted sessions continue where they stopped, without re-downloading media.
- **Smart filtering**: hidden files, BIOS files (`[BIOS]` sets and `bios/` folders) and non-ROM files are automatically excluded.
- Generates `gamelist.xml` in the EmulationStation format used by Batocera, RetroPie, Recalbox, Knulli, EmuELEC and others.

### 🔎 Frontend Detection
Automatically identifies which frontend your ROM folder belongs to by scanning its structure and marker files: **Batocera, Knulli, Recalbox, RetroPie, EmulationStation / ES-DE, EmuELEC, LaunchBox, OnionOS, GarlicOS, muOS and Pegasus**.

### 🖼️ Image Renamer
Batch-rename media files to match your ROM names, with fuzzy matching for slightly different names.

### 🔄 XML Converter
Converts raw ScreenScraper XML/DAT files into `gamelist.xml`, with region and language filters.

### ⚙️ Quality of life
- **Live API quota**: see your daily ScreenScraper request usage in the app.
- **Auto-updater**: checks for new releases on startup and updates in one click.
- **Internationalization**: English, Português (Brasil), Español and Français.
- **Modern UI**: dark theme, responsive layout, real-time activity log.

## Getting started

1. Download the installer for your platform from the [latest release](https://github.com/dgateles/retrotool/releases/latest).
2. (Recommended) Add your [ScreenScraper](https://www.screenscraper.fr) account in **Settings** for higher API quotas and faster scraping.
3. Select your ROMs folder and press **Start**.

## Tech stack

- [Tauri 2](https://v2.tauri.app) (Rust backend: hashing, file operations, ScreenScraper client)
- [React 19](https://react.dev) + [Tailwind CSS 4](https://tailwindcss.com) (frontend)
- [i18next](https://www.i18next.com) (internationalization)

## Acknowledgements

- [ScreenScraper.fr](https://www.screenscraper.fr) and its community for the game metadata database. Consider [supporting them](https://www.screenscraper.fr/aidesupport.php).

