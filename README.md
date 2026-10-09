# VS Code Custom Themes

A collection of six VS Code color themes by MJY, designed for readable syntax highlighting and focused coding sessions across dark and light environments.

## Themes

| Theme | Type | Editor background | Palette |
| --- | --- | --- | --- |
| **Blue Night (MJY)** | Dark | `#282840` | Cyan, neon green, lavender, and warm gold accents |
| **Dark Night (MJY)** | Dark | `#242424` | Neutral charcoal UI with cyan, mint, blue, lavender, and soft teal syntax colors |
| **Dark Night Modern (MJY)** | Dark | `#242424` | Dark Night UI with VS Code Dark Modern text and syntax colors |
| **Blue Day (MJY)** | Light | `#FFFFFF` | High-contrast blue, green, indigo, and purple syntax colors with refined neutral text |
| **Blue Day Modern (MJY)** | Light | `#FFFFFF` | Blue Day UI with Light Modern foreground and syntax colors |
| **Red Day (MJY)** | Light | `#FFFFFF` | VS Code Light+ syntax colors with Blue Day UI colors |

All six themes include semantic token colors and six-color bracket pair highlighting. They are suitable for JavaScript, TypeScript, Python, Java, and other languages supported by VS Code's syntax grammars.

### Dark Night (MJY) visual system

`Dark Night (MJY)` and `Dark Night Modern (MJY)` use `#242424` as their main editor and UI background. Active surfaces use `#2D2D2E`, while inactive editor tabs remain `#242424`. The active tab is marked with a cyan top border (`#89DDFF`), Explorer hover uses `#242626`, and Explorer selection uses `#2D2D2E` whether or not the Explorer has focus.

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

`Dark Night Modern (MJY)` uses the same comment and string colors: comments and Python docstrings use `#8D98B7`, while strings use `#94FEBF`.

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
   - `Dark Night Modern (MJY)`
   - `Blue Day (MJY)`
   - `Blue Day Modern (MJY)`
   - `Red Day (MJY)`

You can also install a locally built package from a terminal:

```sh
code --install-extension vscode-custom-themes-*.vsix
```

## Development

1. Clone this repository and open it in VS Code.
2. Press `F5` to launch an Extension Development Host.
3. Open **Preferences: Color Theme**.
4. Select `Blue Night (MJY)`, `Dark Night (MJY)`, `Dark Night Modern (MJY)`, `Blue Day (MJY)`, `Blue Day Modern (MJY)`, or `Red Day (MJY)`.

Theme definitions live in the `themes/` directory:

- `themes/night-mjy-color-theme.json` — Blue Night (MJY)
- `themes/dark-modern-mjy-color-theme.json` — Dark Night (MJY)
- `themes/dark-night-modern-mjy-color-theme.json` — Dark Night Modern (MJY)
- `themes/day-mjy-color-theme.json` — Blue Day (MJY)
- `themes/blue-modern-day-mjy-color-theme.json` — Blue Day Modern (MJY)
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
