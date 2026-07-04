# aliveos-assets

Distro identity assets for AliveOS: wallpapers and system logo.

## Layout (mirrors install paths)

| Source path | Install path | Contents |
|---|---|---|
| `pixmaps/aliveos-logo.png` | `/usr/share/pixmaps/aliveos-logo.png` | Standalone system logo (referenced by `org.cinnamon system-icon` and login managers) |
| `backgrounds/aliveos/` | `/usr/share/backgrounds/aliveos/` | Default wallpapers in 6 variants: `default.png` (master), 1280×720, 1920×1080, 2560×1440, 3:2, 4:3 |

## Building

```bash
makepkg -si
```