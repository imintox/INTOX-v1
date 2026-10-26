[prettier-badge]: https://img.shields.io/badge/code_style-prettier-ff69b4.svg?style=flat-square
[prettier-link]: https://github.com/prettier/prettier
[sass-badge]: https://img.shields.io/badge/Sass-CC6699.svg?style=flat-square&logo=sass&logoColor=white
[sass-link]: https://sass-lang.com/

<div align="center">

# INTOX

[![code style: prettier][prettier-badge]][prettier-link]
[![Language: Sass][sass-badge]][sass-link]

![INTOX preview](https://files.catbox.moe/9pvwts.png)

</div>

### Features
- Supports visual refresh - New UI with new chat input & new UI with old chat input
- Supports both light and dark, along with dark variants
- Supports saturation setting
- Uses smallest css target possible
- Plugin support in extra files for respective client mods

## Installing

### Vencord (online, always up to date)

1. Open Discord, then go to **Settings → Vencord → Themes**.
2. Paste this link into the **Online Themes** box:

```
https://raw.githubusercontent.com/selfmadegrave/INTOXBlackout-v1/main/INTOX-Online.css
```

3. Enable INTOX in the list, then press `Ctrl+R` to reload Discord.

### Vencord or BetterDiscord (download)

Download a theme file from this repo and move it into your themes folder:

- `INTOX-Vencord.css` for Vencord: `%appdata%\vencord\themes`
- `INTOX-BetterDiscord.theme.css` for BetterDiscord: `%appdata%\betterdiscord\themes`

## Customizing

To change colors, the background, fonts and more, paste [`INTOX-Customize.css`](https://github.com/selfmadegrave/INTOXBlackout-v1/blob/main/INTOX-Customize.css) into Vencord's QuickCSS:

1. Copy everything in `INTOX-Customize.css`.
2. In Discord, go to **Settings → Vencord → Themes → Edit QuickCSS** and paste it at the bottom.
3. Change the values you want. Delete any lines you don't want to change.

Example:

```css
:root {
  --main-color: red;
  --hover-color: yellow;
  --background-size: cover; /* fill the window instead of fitting the whole image */
}
```

## Building from source

To build the theme from source, first install npm from the dependencies below, then you can run `pnpm install` to install all missing dependencies and `pnpm run build` to compile the theme into the `/public` folder.

### Dependencies

- [NodeJS/npm](https://nodejs.org/)
- [pnpm](https://www.npmjs.com/package/pnpm)
- [sass](https://www.npmjs.com/package/sass)
- [PostCSS Autoprefixer](https://www.npmjs.com/package/autoprefixer)
- [PostCSS CLI](https://www.npmjs.com/package/postcss-cli)

## Contributing

Run `pnpm run test` to compile the theme.

The `main.css` file builds to the `/test` directory, which can then be copied into your client mod's Custom CSS or placed in the themes folder and enabled in settings. Just make sure any other themes are disabled for testing.

## Credits

INTOX is a modified fork of [ClearVision v7](https://github.com/ClearVision/ClearVision-v7) by the ClearVision Team, licensed under Apache-2.0 (see `LICENSE` and `NOTICE`).
