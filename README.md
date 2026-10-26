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

Note: INTOX doesn't actively support plugins (as in, we don't seek out and actively theme fixes to every new plugin). However, when a plugin is widely used, we try our best to stay compatible.

**For BD and Vencord:**

Download the theme file from the releases page of this repo and move it into your injector's themes folder:

- BetterDiscord: `%appdata%\betterdiscord\themes`
- Vencord: `%appdata%\vencord\themes`

**For using the theme online:**

Host the built files (GitHub Pages works) and point your client at `main.css`.

For customizing the theme from there, you'll want to use custom css and add any variables you'd like to change. It should look something like this:

```
:root {
	--main-color: red;
	--hover-color: yellow;
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
