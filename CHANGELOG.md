# Changelog

All notable changes to the **Cool Desktop Wallpapers** collection are documented here.

This project has no tags or releases. Changes are tracked by commit on `main`.

---

## 2026-02-21 -- Licensing and repository presentation

### Licensing

- Replaced the plain MIT license with **MIT + OpenAI/Anthropic Rider**, which restricts use by OpenAI, Anthropic, their affiliates, and anyone acting on their behalf without express written permission from Jeffrey Emanuel. The rider covers copying, training, benchmarking, indexing, and all derivative works, with automatic termination on breach.
  ([`903977f`](https://github.com/Dicklesworthstone/cool_desktop_wallpapers/commit/903977f17d21b42502cdc226f36ced01ee590635))

### Social preview

- Added GitHub Open Graph social preview image (`gh_og_share_image.png`, 1280x640) so that links to the repository render a branded card on social media and chat platforms.
  ([`7802dea`](https://github.com/Dicklesworthstone/cool_desktop_wallpapers/commit/7802dea7d6515057c681cda4b1c64bfa1fdf6f2c))

---

## 2026-01-21 -- MIT license added

### Licensing

- Added initial MIT License (Copyright 2026 Jeffrey Emanuel), formalizing open-source terms for the collection.
  ([`bd5e309`](https://github.com/Dicklesworthstone/cool_desktop_wallpapers/commit/bd5e30919149e0b6a40031dfbc3973c585594144))

---

## 2025-12-14 -- Initial collection and Hyprland integration

### Wallpaper collection (9 images, Hiroshi Nagai / citypop aesthetic via Midjourney)

All images depict historical cities and sacred sites rendered in the distinctive style of Hiroshi Nagai -- dreamy, nostalgic citypop art with clean lines, vibrant colors, and serene summer atmosphere. All are high resolution, suitable for 4K-6K displays.

- `cajamarca.png` -- Cajamarca, Peru circa 1500s (~8.7 MB)
- `potosi.png` -- Potosi, Bolivia circa 1650 (~5.6 MB)
- `seville.png` -- Seville, Spain circa 1509 (~4.8 MB)
- `tenochtitlan-1.png` through `tenochtitlan-4.png` -- Tenochtitlan, Aztec Empire (~5.1-7.3 MB each)
- `temple-1.png` and `temple-2.png` -- The First Temple of Jerusalem (~4.7-5.0 MB each)
  ([`1d8d338`](https://github.com/Dicklesworthstone/cool_desktop_wallpapers/commit/1d8d338a3153fa52a4496ed8a9c643d543d2f6b1))

### Curation

- Removed `wallhaven.png` (~40 MB), a non-Midjourney wallpaper sourced from Wallhaven, to keep the collection thematically consistent with the Hiroshi Nagai aesthetic.
  ([`6f0d0de`](https://github.com/Dicklesworthstone/cool_desktop_wallpapers/commit/6f0d0de6204c232480f9b18398485a4d158d02b6))

### Hyprland auto-rotation setup

- Added complete Hyprland wallpaper rotation instructions to the README: a `swww`-based bash rotation script (`rotate.sh`), a systemd user service, and a systemd timer that cycles wallpapers every 2 hours with a grow transition effect. Includes clone, install, enable, and immediate-trigger steps.
  ([`96035ff`](https://github.com/Dicklesworthstone/cool_desktop_wallpapers/commit/96035ffbec5ec29427a084f775640c0a2ecc2b49))

### Project scaffolding

- Added README with wallpaper catalog, image descriptions, resolution notes, and usage guidance.
- Added `.gitignore` excluding `rotate.sh` (generated locally by the setup instructions).
  ([`1d8d338`](https://github.com/Dicklesworthstone/cool_desktop_wallpapers/commit/1d8d338a3153fa52a4496ed8a9c643d543d2f6b1))
