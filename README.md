# Codex Pets

Custom desktop pet packs for Codex—shipping lossless v2 WebP sprite sheets, animation previews, and ready-to-install ZIP archives.

English · [简体中文](README.zh-CN.md)

## Collection

| Hui (`hui-line-fish`) | Miyamori Aoi — At Work (`miyamori-aoi`) | Run, Myaamori! (`run-myaamori`) |
| :---: | :---: | :---: |
| <img src="pets/hui-line-fish/preview.png" alt="Hui white-line fish preview" width="180"> | <img src="pets/miyamori-aoi/preview.gif" alt="Miyamori Aoi idle animation" width="180"> | <img src="pets/run-myaamori/preview.gif" alt="Run Myaamori running animation" width="180"> |
| Minimalist white-line swimming fish on an alpha canvas | Blue work jacket, donut in hand, focused desk companion | Coral jacket, clutching key-frame envelopes on the run |
| [Details](pets/hui-line-fish/) · [ZIP](downloads/hui-line-fish.zip) | [Details](pets/miyamori-aoi/) · [ZIP](downloads/miyamori-aoi.zip) | [Details](pets/run-myaamori/) · [ZIP](downloads/run-myaamori.zip) |

## Installation

1. Download a pet's ZIP archive from the table above and extract its `<pet-id>/` folder.
2. Move `<pet-id>/` into your Codex pets directory (`~/.codex/pets/` on macOS/Linux, `%USERPROFILE%\.codex\pets\` on Windows, or `$CODEX_HOME/pets/`).
3. Open **Settings → Pets** in Codex, refresh the list, and select the pet.

Keep `pet.json` and `spritesheet.webp` in the same directory so `spritesheetPath` resolves:

```text
~/.codex/pets/
└── run-myaamori/
    ├── pet.json
    └── spritesheet.webp
```

## Sprite Format & Repository Layout

Every pet conforms to **Codex sprite format v2**: a lossless RGBA WebP atlas at `1536 × 2288` px (`8` columns × `11` rows, `192 × 208` px per frame) covering 9 standard state animations and 16 gaze directions.

```text
pets/<pet-id>/          Per-pet manifest (pet.json), spritesheet.webp, preview, and notes
downloads/<pet-id>.zip  Ready-to-extract installation archive for each pet
catalog.json            Collection index with dimensions, preview paths, and SHA-256 digests
```

To add a new pet, place its `pet.json`, `spritesheet.webp`, preview image, and `README.md` under `pets/<pet-id>/`, package `downloads/<pet-id>.zip`, and register its entry in [catalog.json](catalog.json). Root-level `pet.json`, `spritesheet.webp`, and `preview.png` are retained for backward compatibility with legacy `hui-line-fish` links.

## Notes

`miyamori-aoi` and `run-myaamori` are fan-made chibi tributes inspired by Aoi Miyamori from the anime *Shirobako*, created with AI-assisted illustration and custom sprite assembly.
