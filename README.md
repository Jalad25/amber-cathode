> [!important]
> Fork of [Amber Cathode](https://www.kindler-webservices.de) by Björn Kindler. See [LICENSE](LICENSE).

# Amber Cathode Extended

An Obsidian dark theme inspired by 80s amber CRT monitors and BBS (Bulletin Board System) aesthetics. This is an extended fork of [Amber Cathode](https://www.kindler-webservices.de) adding switchable phosphor palettes, full-window CRT effects, theme-wide styling, and live controls via the Theme PADD plugin.

![Amber Cathode Extended Screenshot](screenshot_full.png)

## Features

- **Multiple phosphor palettes** — switch between four authentic CRT phosphors:
  - **Amber (P3)** — the classic amber terminal (default)
  - **Green (P1)** — the iconic yellow-green "green screen"
  - **Paper White (P4)** — monochrome black-and-white monitor
  - **Blue-White (P7)** — blue flash with yellow-green persistence
- **Full-window CRT effects** — applied across the *entire* app, not just notes, all simulating an electron beam raster:
  - **Scanlines** — horizontal line overlay simulating the raster line structure
  - **Running line** — a rolling band simulating the electron beam's vertical retrace sweep
  - **Flicker** — a subtle full-window opacity flutter for tube instability
- **Phosphor glow** — warm text-shadow glow on all text, with an adjustable intensity dial
- **Screen vignette & grain** — edge darkening and SVG noise simulating barrel distortion and dot pitch
- **RGB sub-pixel texture** — faint screen-door color separation
- **Full environmental immersion** — modals, settings, side panels, and plugin views all match the theme
- **Full monospace** — VT323 / IBM Plex Mono / JetBrains Mono throughout
- **Sharp corners** — zero border-radius app-wide for a true terminal feel
- **Palette-aware images** — images are tinted to the active phosphor color
- **BBS-themed demo** — includes a showcase file with ASCII art, BASIC code, and retro content

## Installation

1. Download `theme.css` and `manifest.json`
2. Create a folder called `Amber Cathode Extended` in your vault's `.obsidian/themes/` directory
3. Place the files inside
4. Activate the theme in Settings → Appearance

## Customization

### With the Theme PADD plugin

Install the [Theme PADD](https://github.com/Jalad25/theme-padd) plugin and it will load this theme's controls from the repo automatically — no editing required. It exposes:

- **Phosphor palette** — Amber / Green / Paper White / Blue-White
- **Phosphor glow** — `0` (off) to `1` (full)
- **Toggle CRT scanlines, running line, and flicker** independently

### By editing the CSS

All of the theme's behaviour is driven by CSS-variable "knobs" defined near the top of `theme.css`. Edit them directly (or override them in an Obsidian CSS snippet):

| Variable | Controls |
|---|---|
| `--amber-cathode-glow` | Glow intensity (`0`–`1`) |
| `--amber-cathode-bold` | Bold font weight |
| `--amber-cathode-scanline-gap` | Space between scanlines |
| `--amber-cathode-scanline-thickness` | Scanline width |
| `--amber-cathode-scanline-opacity` | Scanline darkness |
| `--amber-cathode-vsync-opacity` | Running line prominence |
| `--amber-cathode-vsync-height` | Running line band height |
| `--amber-cathode-vsync-speed` | Running line sweep duration |

To switch palettes manually, add the matching class to `<body>` via a snippet:

| Palette | Class |
|---|---|
| Amber (P3) | *(default — no class)* |
| Green (P1) | `amber-cathode-green` |
| Paper White (P4) | `amber-cathode-white` |
| Blue-White (P7) | `amber-cathode-blue` |

To disable an individual CRT effect, add the matching class to `<body>`:

| Effect off | Class |
|---|---|
| Scanlines | `amber-cathode-no-scanlines` |
| Running line | `amber-cathode-no-vsync` |
| Flicker | `amber-cathode-no-flicker` |

## Colour Palette (Amber / P3 default)

| Role | Hex |
|---|---|
| Phosphor Bright | `#ffb000` |
| Phosphor Normal | `#cc8800` |
| Phosphor Muted | `#8a5e10` |
| Phosphor Dim | `#5a3e0a` |
| Screen Black | `#0c0a04` |
| Sidebar | `#060400` |
| Border | `#2a2208` |

## Credits

Originally created by [Björn Kindler](https://www.kindler-webservices.de). This fork extends it with additional palettes, effects, and plugin integration.

## License

MIT License — see [LICENSE](LICENSE)
