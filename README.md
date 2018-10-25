# Glyphs Resources
A collection of resources for Glyphs App

# Table of Contents

## Script Collections
- [Eli Heuer](https://github.com/eliheuer/vanilla-free-glyphs-scripts)
- [Google Fonts](https://github.com/googlefonts/gf-glyphs-scripts)
- [Guido Ferreyra](https://github.com/guidoferreyra/Glyphs-Scripts)
- [Huerta Tipografica](https://github.com/huertatipografica/huertatipografica-scripts)
- [Jens Kutilek](https://github.com/jenskutilek/Glyphs-Scripts)
- [Just Another Foundry](https://github.com/justanotherfoundry/font-production)
- [Marc Foley](https://github.com/m4rc1e/mf-glyphs-scripts)
- [Marcin Dybaś](https://github.com/dyyybek/Glyphs-Scripts)
- [Mark Fromberg](https://github.com/Mark2Mark/Glyphsapp-Scripts-Free)
- [Mekkablue (Rainer Erich Scheichelbauer)](https://github.com/mekkablue/Glyphs-Scripts)
- [Mike LaGattuta](https://github.com/mjlagattuta/Glyphs-Scripts)
- [Simon Cozens](https://github.com/simoncozens/GlyphsScripts)
- [Stephen Nixon](https://github.com/thundernixon/glyphs_scripts)
- [Tosche](https://github.com/Tosche/Glyphs-Scripts)
- [Wei Huang](https://github.com/weiweihuanghuang/wei-glyphs-scripts)

## Hacks (This needs a better name)
### Hide Metrics in Text View
When the text tool is selected, the side-bearing values are visible beneath each glyph. By default, these metrics are hidden when the text is viewed at 75pt or smaller. To hide them at larger sizes, run the code below in the Macro panel. In this example, the metrics will be hidden at any size under 151pt.

`Glyphs.intDefaults["TextModeNumbersThreshold"] = 151`

