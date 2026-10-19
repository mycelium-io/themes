# Mycelium themes

Color themes for the [Mycelium](https://github.com/mycelium-io/mycelium) app. Each theme is one small JSON file, and you can install any of them with one command.

## Install a theme

```bash
mycelium theme add https://raw.githubusercontent.com/mycelium-io/themes/main/themes/moss.json --use
```

`--use` switches the app to the theme right away. Leave it off to just add the theme, then pick it later with `mycelium theme use <name>` or from the app's theme picker. `mycelium theme ls` lists what you have, and `mycelium theme rm <name>` removes one.

Themes are files on your own machine (in `~/.mycelium/themes/`), not settings on a hub, so a theme you add is yours and nobody else in your rooms sees it.

## The themes

Made for Mycelium:

| Theme | Mode | File |
| --- | --- | --- |
| Amber CRT | dark | [`amber-crt.json`](themes/amber-crt.json) |
| Bioluminescence | dark | [`bioluminescence.json`](themes/bioluminescence.json) |
| Lavender Dusk | dark | [`lavender-dusk.json`](themes/lavender-dusk.json) |
| Moss | dark | [`moss.json`](themes/moss.json) |
| Risograph | light | [`risograph.json`](themes/risograph.json) |

The app's built-in themes, as files. The app already has these, so you only need them as a starting point for your own:

| Theme | Mode | File |
| --- | --- | --- |
| Mycelium light | light | [`mycelium-light.json`](themes/mycelium-light.json) |
| Mycelium dark | dark | [`mycelium-dark.json`](themes/mycelium-dark.json) |
| Catppuccin Latte | light | [`catppuccin-latte.json`](themes/catppuccin-latte.json) |
| Catppuccin Mocha | dark | [`catppuccin-mocha.json`](themes/catppuccin-mocha.json) |
| Dracula | dark | [`dracula.json`](themes/dracula.json) |
| GitHub light | light | [`github-light.json`](themes/github-light.json) |
| GitHub dark | dark | [`github-dark.json`](themes/github-dark.json) |
| Gruvbox light | light | [`gruvbox-light.json`](themes/gruvbox-light.json) |
| Gruvbox dark | dark | [`gruvbox-dark.json`](themes/gruvbox-dark.json) |
| High contrast light | light | [`high-contrast-light.json`](themes/high-contrast-light.json) |
| High contrast dark | dark | [`high-contrast-dark.json`](themes/high-contrast-dark.json) |
| Nord | dark | [`nord.json`](themes/nord.json) |
| One Dark | dark | [`one-dark.json`](themes/one-dark.json) |
| Solarized light | light | [`solarized-light.json`](themes/solarized-light.json) |
| Solarized dark | dark | [`solarized-dark.json`](themes/solarized-dark.json) |
| Tokyo Night | dark | [`tokyo-night.json`](themes/tokyo-night.json) |

## Make your own

Copy the theme closest to what you want, change its `name` and colors, and add it with `mycelium theme add my-theme.json --use`. A theme looks like this:

```json
{
  "name": "Moss",
  "mode": "dark",
  "colors": {
    "bg": "#11140f",
    "text": "#e7ecdc",
    "accent": "#b5d66b",
    "...": "..."
  }
}
```

- `mode` is `light` or `dark`, and decides which way the app's few fixed colors lean.
- These colors are required: `bg`, `surface`, `paper`, `elevated`, `muted-bg`, `text`, `muted-foreground`, `faint`, `accent`, `accent-fg`, `green`, `yellow` and `red`.
- These are optional: `prose`, `border`, `border2`, `hairline`, `accent-soft` and `avatar-ink`.
- Colors are hex (`#rgb` or `#rrggbb`). Only `border`, `border2`, `hairline` and `accent-soft` may be see-through (`#rrggbbaa`).

The app checks a theme's contrast when you pick it and tells you which pairs are hard to read. Every theme here meets WCAG AA (4.5:1) for text, prose, muted and faint text on every background, the accent on the main backgrounds, the status colors on the backgrounds they sit on, and `accent-fg` on `accent`.

To add a theme to this repo, open a pull request with its file in `themes/` and a row in the table above.

## Credits

The built-in themes are Mycelium's versions of palettes made by others: [Catppuccin](https://github.com/catppuccin/catppuccin), [Dracula](https://draculatheme.com), [GitHub's Primer](https://primer.style), [Gruvbox](https://github.com/morhetz/gruvbox), [Nord](https://www.nordtheme.com), [One Dark](https://github.com/atom/atom/tree/master/packages/one-dark-ui), [Solarized](https://ethanschoonover.com/solarized/) and [Tokyo Night](https://github.com/enkia/tokyo-night-vscode-theme). Some colors are adjusted to meet the contrast rules above.

## License

Apache 2.0, the same as Mycelium.
