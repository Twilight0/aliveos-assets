# aliveos-assets

Distro identity assets for AliveOS: neon dark square icon theme, wallpapers, and system logo.

## Layout (mirrors install paths)

| Source path | Install path | Contents |
|---|---|---|
| `icons/aliveos/` | `/usr/share/icons/aliveos/` | Icon theme: 212 base PNGs + 812 symlinks across 7 sizes (16, 22, 32, 48, 64, 128, 256) × 7 contexts (apps, places, actions, devices, mimetypes, preferences, status) + `index.theme` |
| `pixmaps/aliveos-logo.png` | `/usr/share/pixmaps/aliveos-logo.png` | Standalone system logo (referenced by `org.cinnamon system-icon` and login managers) |
| `backgrounds/aliveos/` | `/usr/share/backgrounds/aliveos/` | Default wallpapers in 6 variants: `default.png` (master), 1280×720, 1920×1080, 2560×1440, 3:2, 4:3 |

## Icon theme specifics

- Inherits: `Papirus-Dark,Adwaita,hicolor` (Papirus-Dark recommended as optdep in the installing PKGBUILD)
- Theme name: `aliveos`
- Style: neon dark square — flat-design square icons with neon accents
- Generated via the scripts in `aliveos/` project (`scripts/rebuild_*.py`)

## Building

```bash
makepkg -si
```

## Installing on non-AliveOS Arch

Requires `hicolor-icon-theme`. Optionally install `papirus-icon-theme` for fallback icons not present in the aliveos set.