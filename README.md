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
- Minimalist black look with a single calm accent color
- Clean, quick animations (menus, hover toolbar, focus) that turn off with `--intox-speed: 0ms` and follow your system's "reduce motion" setting
- Glass-blur popouts and windows with hairline edges
- Quiet scrollbars that hide in the channel and member lists until you hover
- Fixed background image that never crops when you resize the window
- Optional extras, all off until you turn them on: multi-column server list, more animation styles, hover effects, hiding parts of Discord you don't use (Nitro, Shop, Quests, Active Now, Message Requests, Family Center, the Add a Server/Discover/Download Apps buttons, Help and the gift button), flat (glow-free) unread items, a background vignette and accent text selection
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
https://raw.githubusercontent.com/imintox/INTOX-v1/main/INTOX-Online.css
```

3. Enable INTOX in the list, then press `Ctrl+R` to reload Discord.

### Vencord or BetterDiscord (download)

Download a theme file from this repo and move it into your themes folder:

- `INTOX-Vencord.css` for Vencord: `%appdata%\vencord\themes`
- `INTOX-BetterDiscord.theme.css` for BetterDiscord: `%appdata%\betterdiscord\themes`

## Editor

Build your own look with the live editor, then copy the CSS into Vencord's QuickCSS:

**https://imintox.github.io/INTOX-Editor/**

## Customizing

To change colors, the background, fonts and more, paste [`INTOX-Customize.css`](https://github.com/imintox/INTOX-v1/blob/main/INTOX-Customize.css) into Vencord's QuickCSS:

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

## Optional features

Everything below is **off by default**. Turn a feature on in QuickCSS (or with the [editor](https://imintox.github.io/INTOX-Editor/)), for example:

```css
:root {
  --intox-server-columns: 2;      /* server list in 2 columns, home stays centered (1-4, experimental) */
  --intox-menu-anim: intox-pop;   /* menus: intox-rise, intox-fade, intox-pop, intox-slide, intox-drop or none */
  --intox-hide-shop: on;          /* switches use "on" */
}
```

| Setting | What it does |
|---|---|
| `--intox-server-columns` | `1`-`4` columns in the server list (experimental) |
| `--intox-menu-anim` | Menu animation (default `intox-rise`) |
| `--intox-toolbar-anim` | Message hover toolbar animation (default `intox-fade`) |
| `--intox-window-anim` | Window animation (default `none`) |
| `--intox-message-anim` | New message animation (default `none`) |
| `--intox-bg-anim` / `--intox-bg-speed` | Background motion: `intox-drift` or `intox-breathe`, seconds per loop |
| `--intox-hover-servers` / `-channels` / `-avatars` | Hover effects |
| `--intox-hide-nitro` / `-shop` / `-quests` / `-active-now` | Hide those parts of Discord |
| `--intox-hide-requests` / `-family` | Hide the Message Requests and Family Center links |
| `--intox-hide-add-server` / `-discover` / `-download` | Hide the buttons at the bottom of the server list |
| `--intox-hide-help` | Hide the Help (?) button at the top right |
| `--intox-hide-gift` | Hide the gift button in the message box (English Discord only) |
| `--intox-no-glow` | Remove glows on unread items |
| `--intox-vignette` | Darker edges around the background |
| `--intox-selection` | Accent-colored text selection |

All INTOX motion stays off when your system asks to reduce motion. The links are matched by where they go, so hiding works in every Discord language. Switches rely on CSS style queries, which Discord's desktop app supports; where they aren't supported, the feature simply stays off.

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
