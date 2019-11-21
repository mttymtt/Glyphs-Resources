# Glyphs Resources
A collection of resources for Glyphs App

# Table of Contents
- [Tips & Tricks](#tips--tricks)
- [Script Collections](#script-collections)
- [Small Scripts/Hacks](#small-scriptshacks)

---

## Tips & Tricks

**Table of Contents**
- [Display All Cooridinates](#display-all-cooridinates)
- [Draw Guide from Measurement Tool](#draw-guide-from-measurement-tool)
- [Regenerate Components Inside of Component Glyph](#regenerate-components-inside-of-component-glyph)

### Display All Cooridinates
- Hold down `Control + Option + Command`
- Alternatively, switch to the measurement tool (L)

### Draw Guide from Measurement Tool
- While using the measurement tool (L), press `G` to create a guide.

### Regenerate Components Inside of Component Glyph
- `Shift + Option + Command + C` or Glyph > Make Component Glyph
- Imagine you have an empty /Aacute glyph, but have drawn the /A and the /acutecomb, this will automatically generate them back into the /Aacute glyph
- Extra hot tip: You can select multiple glyphs at once and do this. So if you added your combining diacritic characters before drawing all of your necessary components, there’s no need to individually place components later on.

---

## Script Collections
- [Alexei Vanyashin](https://github.com/alexeiva/alexei-scripts)
- [Daniel Gamage](https://github.com/danielgamage/Glyphs-Scripts)
- [Eli Heuer](https://github.com/eliheuer/vanilla-free-glyphs-scripts)
- [Ethan Cohen](https://github.com/ethancohen/Misc-Glyphs-Scripts)
- [Felipe Negrão](https://github.com/filipenegrao/glyphsapp-scripts)
- [Georg Seifert](https://github.com/schriftgestalt/Glyphs-Scripts)
- [Google Fonts](https://github.com/googlefonts/gf-glyphs-scripts)
- [Guido Ferreyra](https://github.com/guidoferreyra/Glyphs-Scripts)
- [Harbor Type](https://github.com/harbortype/glyphs-scripts)
- [Huerta Tipografica](https://github.com/huertatipografica/huertatipografica-scripts)
- [Jens Kutilek](https://github.com/jenskutilek/Glyphs-Scripts)
- [Just Another Foundry - Freemix](https://github.com/justanotherfoundry/freemix-glyphsapp)
- [Just Another Foundry - Font Production](https://github.com/justanotherfoundry/font-production)
- [Kyle Wayne Benson](https://github.com/kylewaynebenson/Glyphs-Scripts)
- [Marc Foley](https://github.com/m4rc1e/mf-glyphs-scripts)
- [Marcin Dybaś](https://github.com/dyyybek/Glyphs-Scripts)
- [Mark Fromberg](https://github.com/Mark2Mark/Glyphsapp-Scripts-Free)
- [Mekkablue (Rainer Erich Scheichelbauer)](https://github.com/mekkablue/Glyphs-Scripts)
- [Mike LaGattuta](https://github.com/mjlagattuta/Glyphs-Scripts)
- [Olli Meier](https://github.com/moontypespace/omScripts)
- [Pedro Arilla](https://github.com/pedroarilla/glyphs-scripts)
- [Robert Janes](https://github.com/robertjanes/Glyphs-Scripts)
- [Simon Cozens](https://github.com/simoncozens/GlyphsScripts)
- [Stephen Nixon](https://github.com/thundernixon/glyphs_scripts)
- [Tosche](https://github.com/Tosche/Glyphs-Scripts)
- [Wei Huang](https://github.com/weiweihuanghuang/wei-glyphs-scripts)

---

## Small Scripts/Hacks
These are small scripts you can run in the macro panel to do various things inside of Glyphs. Most often, they have to do with how Glyphs performs as opposed to editing your actual work.

**Table of Contents**
- [Change Macro Panel Font Size](#change-macro-panel-font-size)
- [Export Instances as UFOs](#export-instances-as-ufos)
- [Fetch Names and Unicode values of all Glyphs in Font](#fetch-names-and-unicode-values-of-all-glyphs-in-font)
- [Hide Metrics in Text View](#hide-metrics-in-text-view)
- [Name Guideline](#name-guideline)
- [Save Vector Screenshot of Glyphs Window](#save-vector-screenshot-of-glyphs-window)

### Change Macro Panel Font Size
Fairly straight forward. 12 in the example below represents the font size.

```
Glyphs.intDefaults["MacroCodeFontSize"] = 12
```

### Export Instances as UFOs
Glyphs built-in export as UFOs option only exports the masters, so if you need to export all of the instances or certain instances as UFOs, you can use the following script:

```
import os
for instance in Font.instances:
	instance.generate(UFO, os.path.expanduser("~/Desktop"))
```

There are two more options `UseProductionNames (default True)` and `DecomposeSmartStuff (default True)`. In which case, the code would look like:

```
import os
for instance in Font.instances:
    instance.generate(UFO, os.path.expanduser("~/Desktop"), UseProductionNames=False, DecomposeSmartStuff=False)
```



### Fetch Names and Unicode values of all Glyphs in Font

```
font = Glyphs.font

for i in font.glyphs:
    if i.unicode:
        print i.name + " - " + i.unicode
```

### Hide Metrics in Text View
When the text tool is selected, the side-bearing values are visible beneath each glyph. By default, these metrics are hidden when the text is viewed at 75pt or smaller. To hide them at larger sizes, run the code below in the Macro panel. In this example, the metrics will be hidden at any size under 151pt.

```
Glyphs.intDefaults["TextModeNumbersThreshold"] = 151
```

### Name Guideline
This will add a name to your guideline. Just select one guideline, then run the script in the macro panel.

```
Layer.selection[0].name = "Guide Name Here"
```

### Save Vector Screenshot of Glyphs Window
This prompts a print dialog box for your Glyphs Window. Click on “PDF” in the lower left hand corner and then choose “Save as PDF.”

```
Font.currentTab.graphicView().window().print_(None)
```
