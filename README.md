# VS Code Custom Themes

A collection of five VS Code color themes by MJY, designed for readable syntax highlighting and focused coding sessions across dark and light environments.

## Themes

| Theme | Type | Editor background | Palette |
| --- | --- | --- | --- |
| **Blue Night (MJY)** | Dark | `#292D36` | Cyan, neon green, lavender, and warm gold accents |
| **Black Night (MJY)** | Dark | `#242424` | Black Night UI with VS Code Dark Modern text and syntax colors |
| **Black Night Modern (MJY)** | Dark | `#222222` | Black Night Modern syntax with soft mint strings, light gray variables, muted comments, and lavender type names |
| **Blue Light (MJY)** | Light | `#FFFFFF` | Teal keywords, navy strings, blue symbols, and muted gray comments and docstrings |
| **Blue Light Modern (MJY)** | Light | `#FFFFFF` | Light Modern syntax colors with muted gray comments and docstrings |

All five themes include semantic token colors and six-color bracket pair highlighting. They are suitable for JavaScript, TypeScript, Python, Java, and other languages supported by VS Code's syntax grammars.

### Blue Light comment and string colors

`Blue Light (MJY)` uses teal `#006B76` for keywords, blue `#3B5FA9` for module and namespace semantic tokens, and navy `#0A3069` for strings. Comments and docstrings share the muted gray `#8A9098`.

`Blue Light Modern (MJY)` keeps its Light Modern syntax palette and uses the same muted gray `#8A9098` for comments and docstrings.

### Blue Night (MJY) visual system

`Blue Night (MJY)` uses `#292D36` as its main editor and UI background. Active surfaces use `#353B49`, while hover and focus surfaces use `#3E4656`. The current-line highlight uses `#2F343E` for a subtle neutral contrast.

### Black Night (MJY) visual system

`Black Night (MJY)` uses `#242424` as its main editor and UI background. Active surfaces use `#2D2D2E`, while inactive editor tabs remain `#242424`. The current-line highlight uses `#2A2A2A`. The active tab is marked with a cyan top border (`#89DDFF`), Explorer hover uses `#242626`, and Explorer selection uses `#2D2D2E` whether or not the Explorer has focus.

Its current syntax palette includes:

| Role | Color |
| --- | --- |
| Variables and parameters | `#D6DEE5` |
| Functions | `#78D8E8` |
| Types and classes | `#8FD3FF` |
| Modules and namespaces | `#91B4D5` |
| Strings | `#86D9A8` |
| Control flow (`if`, `for`, `try`, `return`, etc.) | `#C4B5FF` |
| Python function and logical keywords (`def`, `not`, `and`, `lambda`, etc.) | `#8AEDCF` |
| Comments and Python docstrings | `#707887` |
| Warning diagnostics | `#FFD580` |
| Added Git resources | `#A6E3A1` |

Comments and Python docstrings use `#707887`, while strings use `#86D9A8`.

### Black Night Modern (MJY) visual system

`Black Night Modern (MJY)` keeps the built-in Dark Modern syntax palette with a few focused color changes. The code editor uses `#222222`, while the main workbench surfaces use the subtly darker `#202020`.

Its syntax palette distinguishes these roles:

| Role | Color |
| --- | --- |
| Strings | `#98D1AE` |
| General keywords | `#9CDCFE` |
| Functions, methods, and decorators | `#78C7D4` |
| Local variables | `#E6E6E6` |
| Python function parameters | `#85B6FF` |
| Python uppercase constants and enum members | `#F2F2F2` |
| Python language constants (`True`, `False`, `None`) | `#C0C0C0` |
| Comments and Python docstrings | `#858C99` |
| Regex character classes | `#78C7D4` |
| Regex pattern text | `#C4C4C4` |
| Regex groups | `#F2F2F2` |
| Regex operators and escapes | `#C586C0` |
| Types, classes, and exception names | `#B9C4FF` |
| Control-flow keywords | `#C586C0` |

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
   - `Black Night (MJY)`
   - `Black Night Modern (MJY)`
   - `Blue Light (MJY)`
   - `Blue Light Modern (MJY)`

You can also install a locally built package from a terminal:

```sh
code --install-extension vscode-custom-themes-*.vsix
```

## Development

1. Clone this repository and open it in VS Code.
2. Press `F5` to launch an Extension Development Host.
3. Open **Preferences: Color Theme**.
4. Select one of the five themes listed above.

Theme definitions live in the `themes/` directory:

- `themes/blue-night.json` — Blue Night (MJY)
- `themes/black-night.json` — Black Night (MJY)
- `themes/black-night-modern.json` — Black Night Modern (MJY)
- `themes/blue-light.json` — Blue Light (MJY)
- `themes/blue-light-modern.json` — Blue Light Modern (MJY)

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
