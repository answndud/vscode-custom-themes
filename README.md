# VS Code Custom Themes

A collection of five VS Code color themes by MJY, designed for readable syntax highlighting and focused coding sessions across dark and light environments.

## Themes

| Theme | Type | Editor background | Palette |
| --- | --- | --- | --- |
| **Blue Night (MJY)** | Dark | `#282840` | Cyan, neon green, lavender, and warm gold accents |
| **Dark Night (MJY)** | Dark | `#1B1B1C` | Neutral charcoal UI with cyan, mint, blue, lavender, and soft teal syntax colors |
| **Blue Day (MJY)** | Light | `#FFFFFF` | High-contrast blue, green, indigo, and purple syntax colors with refined neutral text |
| **Blue Modern Day (MJY)** | Light | `#FFFFFF` | Blue Day UI with Light Modern foreground and syntax colors |
| **Red Day (MJY)** | Light | `#FFFFFF` | VS Code Light+ syntax colors with Blue Day UI colors |

All five themes include semantic token colors and six-color bracket pair highlighting. They are suitable for JavaScript, TypeScript, Python, Java, and other languages supported by VS Code's syntax grammars.

### Dark Night (MJY) visual system

`Dark Night (MJY)` uses `#1B1B1C` as its main editor and UI background. Active surfaces use `#292929`, while inactive editor tabs remain `#1B1B1C`. The active tab is marked with a cyan top border (`#89DDFF`), Explorer hover uses `#242626`, and inactive Explorer selection uses `#222222`.

Its current syntax palette includes:

| Role | Color |
| --- | --- |
| Variables and parameters | `#F4F7FF` |
| Functions | `#8BE9FD` |
| Types and classes | `#8FD3FF` |
| Modules and namespaces | `#CAF2B6` |
| Strings | `#94FEBF` |
| Control flow (`if`, `for`, `try`, `return`, etc.) | `#78D8C8` |
| Function definition (`def`) | `#E7B8FF` |
| Comments and Python docstrings | `#8D98B7` |
| Warning diagnostics | `#FFD580` |
| Added Git resources | `#A6E3A1` |

The theme files are the source of truth. Do not duplicate these colors in VS Code `workbench.colorCustomizations`, because those settings override the theme.

## Installation

### From the Marketplace

Search for **VS Code Custom Themes** or **vscode-custom-themes** in the VS Code Extensions view after the extension is published.

### From a VSIX file

1. Download the latest `.vsix` file from the repository's Releases page.
2. Open VS Code.
3. Open the Command Palette and run **Extensions: Install from VSIX...**.
4. Select the downloaded file.
5. Run **Preferences: Color Theme** and choose one of:
   - `Blue Night (MJY)`
   - `Dark Night (MJY)`
   - `Blue Day (MJY)`
   - `Blue Modern Day (MJY)`
   - `Red Day (MJY)`

You can also install a locally built package from a terminal:

```sh
code --install-extension vscode-custom-themes-*.vsix
```

## Development

1. Clone this repository and open it in VS Code.
2. Press `F5` to launch an Extension Development Host.
3. Open **Preferences: Color Theme**.
4. Select `Blue Night (MJY)`, `Dark Night (MJY)`, `Blue Day (MJY)`, `Blue Modern Day (MJY)`, or `Red Day (MJY)`.

Theme definitions live in the `themes/` directory:

- `themes/night-mjy-color-theme.json` — Blue Night (MJY)
- `themes/dark-modern-mjy-color-theme.json` — Dark Night (MJY)
- `themes/day-mjy-color-theme.json` — Blue Day (MJY)
- `themes/blue-modern-day-mjy-color-theme.json` — Blue Modern Day (MJY)
- `themes/red-day-mjy-color-theme.json` — Red Day (MJY)

For the personal local installation, keep the installed extension path linked to this repository instead of editing the installed copy:

```sh
ln -sfn "$(pwd)" "$HOME/.vscode/extensions/mjy.vscode-custom-themes-0.4.3"
```

After changing a theme, run **Developer: Reload Window** and reselect the theme if necessary.

## Packaging

Install the VS Code Extension Manager and create a VSIX package:

```sh
npm install -g @vscode/vsce
vsce package
```

The generated VSIX can be installed locally or uploaded to the Visual Studio Marketplace.

## License

MIT
