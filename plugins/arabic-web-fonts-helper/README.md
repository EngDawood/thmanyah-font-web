# Arabic Web Fonts Helper

A Claude skill that helps you add Arabic web fonts to a website or app. It currently covers the community Thmanyah (ثمانية) font package, `@dawod/thmanyah-font-web`, with three families (Sans, Serif Display, Serif Text) in five weights.

When you ask Claude to use Thmanyah or Arabic web fonts, the skill guides it to link the stylesheet or install the npm package, write the right `font-family` and `font-weight` rules, apply the utility classes, and follow an Arabic right-to-left checklist.

## What it does and what it touches

- It only adds instructions to Claude's context. It has no hooks, scripts, MCP servers, or commands, and it does not run anything itself.
- Code it suggests for your project loads a stylesheet from `cdn.jsdelivr.net`, which serves the npm package, or installs `@dawod/thmanyah-font-web` with npm. Your visitors' browsers contact jsDelivr to fetch the font files.
- It sends no data anywhere else and bundles no font files.

## License

This plugin (the skill and README) is MIT licensed, see `LICENSE`. That does not cover the font.

## Font license note

The font belongs to Thmanyah, and its license (https://font.thmanyah.com/licenses) allows personal use and does not authorize redistribution. Check it before using the font in commercial work.

## Links

- Demo: https://engdawood.github.io/thmanyah-font-web/
- Source: https://github.com/engdawood/thmanyah-font-web
