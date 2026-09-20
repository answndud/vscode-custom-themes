# VS Code Custom Themes

A collection of three VS Code color themes by MJY, designed for readable syntax highlighting and focused coding sessions across dark and light environments.

## Themes

| Theme | Type | Editor background | Palette |
| --- | --- | --- | --- |
| **Blue Night (MJY)** | Dark | `#282840` | Cyan, neon green, lavender, and warm gold accents |
| **Dark Night (MJY)** | Dark | `#222426` | Neutral charcoal UI with cyan, mint, blue, and lavender syntax colors |
| **Blue Day (MJY)** | Light | `#FFFFFF` | High-contrast blue, green, indigo, and purple syntax colors with refined neutral text |
| **Red Day (MJY)** | Light | `#FFFFFF` | VS Code Light+ syntax colors with Blue Day UI colors |

All four themes include semantic token colors and six-color bracket pair highlighting. They are suitable for JavaScript, TypeScript, Python, Java, and other languages supported by VS Code's syntax grammars.

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
   - `Red Day (MJY)`

You can also install a locally built package from a terminal:

```sh
code --install-extension vscode-custom-themes-*.vsix
```

## Development

1. Clone this repository and open it in VS Code.
2. Press `F5` to launch an Extension Development Host.
3. Open **Preferences: Color Theme**.
4. Select `Blue Night (MJY)`, `Dark Night (MJY)`, `Blue Day (MJY)`, or `Red Day (MJY)`.

Theme definitions live in the `themes/` directory:

- `themes/night-mjy-color-theme.json` — Blue Night (MJY)
- `themes/dark-modern-mjy-color-theme.json` — Dark Night (MJY)
- `themes/day-mjy-color-theme.json` — Blue Day (MJY)
- `themes/red-day-mjy-color-theme.json` — Red Day (MJY)

## Packaging

Install the VS Code Extension Manager and create a VSIX package:

```sh
npm install -g @vscode/vsce
vsce package
```

The generated VSIX can be installed locally or uploaded to the Visual Studio Marketplace.

## License

MIT
