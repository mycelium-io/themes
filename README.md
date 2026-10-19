# Mycelium themes

Color themes for the [Mycelium](https://github.com/mycelium-io/mycelium) app. Each theme is one small JSON file, and you can install any of them with one command.

## Install a theme

```bash
mycelium theme add https://raw.githubusercontent.com/mycelium-io/themes/main/themes/moss.json --use
```

`--use` switches the app to the theme right away. Leave it off to just add the theme, then pick it later with `mycelium theme use <name>` or from the app's theme picker. `mycelium theme ls` lists what you have, and `mycelium theme rm <name>` removes one.

Themes are files on your own machine (in `~/.mycelium/themes/`), not settings on a hub, so a theme you add is yours and nobody else in your rooms sees it.

## The themes

Each picture is the same room in the app, in that theme. Click a theme's name for its file.

Made for Mycelium:

<table>
<tr><td width="50%"><a href="themes/amber-crt.json"><b>Amber CRT</b></a> · dark<br><a href="screens/amber-crt.png"><img src="screens/amber-crt.png" alt="Mycelium in Amber CRT"></a></td><td width="50%"><a href="themes/bioluminescence.json"><b>Bioluminescence</b></a> · dark<br><a href="screens/bioluminescence.png"><img src="screens/bioluminescence.png" alt="Mycelium in Bioluminescence"></a></td></tr>
<tr><td width="50%"><a href="themes/lavender-dusk.json"><b>Lavender Dusk</b></a> · dark<br><a href="screens/lavender-dusk.png"><img src="screens/lavender-dusk.png" alt="Mycelium in Lavender Dusk"></a></td><td width="50%"><a href="themes/moss.json"><b>Moss</b></a> · dark<br><a href="screens/moss.png"><img src="screens/moss.png" alt="Mycelium in Moss"></a></td></tr>
<tr><td width="50%"><a href="themes/risograph.json"><b>Risograph</b></a> · light<br><a href="screens/risograph.png"><img src="screens/risograph.png" alt="Mycelium in Risograph"></a></td></tr>
</table>

The app's built-in themes, as files. The app already has these, so you only need them as a starting point for your own:

<table>
<tr><td width="50%"><a href="themes/mycelium-light.json"><b>Mycelium light</b></a> · light<br><a href="screens/mycelium-light.png"><img src="screens/mycelium-light.png" alt="Mycelium in Mycelium light"></a></td><td width="50%"><a href="themes/mycelium-dark.json"><b>Mycelium dark</b></a> · dark<br><a href="screens/mycelium-dark.png"><img src="screens/mycelium-dark.png" alt="Mycelium in Mycelium dark"></a></td></tr>
<tr><td width="50%"><a href="themes/catppuccin-latte.json"><b>Catppuccin Latte</b></a> · light<br><a href="screens/catppuccin-latte.png"><img src="screens/catppuccin-latte.png" alt="Mycelium in Catppuccin Latte"></a></td><td width="50%"><a href="themes/catppuccin-mocha.json"><b>Catppuccin Mocha</b></a> · dark<br><a href="screens/catppuccin-mocha.png"><img src="screens/catppuccin-mocha.png" alt="Mycelium in Catppuccin Mocha"></a></td></tr>
<tr><td width="50%"><a href="themes/dracula.json"><b>Dracula</b></a> · dark<br><a href="screens/dracula.png"><img src="screens/dracula.png" alt="Mycelium in Dracula"></a></td><td width="50%"><a href="themes/github-light.json"><b>GitHub light</b></a> · light<br><a href="screens/github-light.png"><img src="screens/github-light.png" alt="Mycelium in GitHub light"></a></td></tr>
<tr><td width="50%"><a href="themes/github-dark.json"><b>GitHub dark</b></a> · dark<br><a href="screens/github-dark.png"><img src="screens/github-dark.png" alt="Mycelium in GitHub dark"></a></td><td width="50%"><a href="themes/gruvbox-light.json"><b>Gruvbox light</b></a> · light<br><a href="screens/gruvbox-light.png"><img src="screens/gruvbox-light.png" alt="Mycelium in Gruvbox light"></a></td></tr>
<tr><td width="50%"><a href="themes/gruvbox-dark.json"><b>Gruvbox dark</b></a> · dark<br><a href="screens/gruvbox-dark.png"><img src="screens/gruvbox-dark.png" alt="Mycelium in Gruvbox dark"></a></td><td width="50%"><a href="themes/high-contrast-light.json"><b>High contrast light</b></a> · light<br><a href="screens/high-contrast-light.png"><img src="screens/high-contrast-light.png" alt="Mycelium in High contrast light"></a></td></tr>
<tr><td width="50%"><a href="themes/high-contrast-dark.json"><b>High contrast dark</b></a> · dark<br><a href="screens/high-contrast-dark.png"><img src="screens/high-contrast-dark.png" alt="Mycelium in High contrast dark"></a></td><td width="50%"><a href="themes/nord.json"><b>Nord</b></a> · dark<br><a href="screens/nord.png"><img src="screens/nord.png" alt="Mycelium in Nord"></a></td></tr>
<tr><td width="50%"><a href="themes/one-dark.json"><b>One Dark</b></a> · dark<br><a href="screens/one-dark.png"><img src="screens/one-dark.png" alt="Mycelium in One Dark"></a></td><td width="50%"><a href="themes/solarized-light.json"><b>Solarized light</b></a> · light<br><a href="screens/solarized-light.png"><img src="screens/solarized-light.png" alt="Mycelium in Solarized light"></a></td></tr>
<tr><td width="50%"><a href="themes/solarized-dark.json"><b>Solarized dark</b></a> · dark<br><a href="screens/solarized-dark.png"><img src="screens/solarized-dark.png" alt="Mycelium in Solarized dark"></a></td><td width="50%"><a href="themes/tokyo-night.json"><b>Tokyo Night</b></a> · dark<br><a href="screens/tokyo-night.png"><img src="screens/tokyo-night.png" alt="Mycelium in Tokyo Night"></a></td></tr>
</table>

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

To add a theme to this repo, open a pull request with its file in `themes/` and a cell for it above. You don't need to take its picture: the pictures in `screens/` are made by Mycelium's screenshot job, which shoots the app in every theme in this repo. To remake them, run `npm run screenshots themes` in Mycelium's `mycelium-frontend`, with this repo checked out next to the Mycelium repo (or `MYCELIUM_THEMES_REPO` set to where it is).

## Credits

The built-in themes are Mycelium's versions of palettes made by others: [Catppuccin](https://github.com/catppuccin/catppuccin), [Dracula](https://draculatheme.com), [GitHub's Primer](https://primer.style), [Gruvbox](https://github.com/morhetz/gruvbox), [Nord](https://www.nordtheme.com), [One Dark](https://github.com/atom/atom/tree/master/packages/one-dark-ui), [Solarized](https://ethanschoonover.com/solarized/) and [Tokyo Night](https://github.com/enkia/tokyo-night-vscode-theme). Some colors are adjusted to meet the contrast rules above.

## License

Apache 2.0, the same as Mycelium.
