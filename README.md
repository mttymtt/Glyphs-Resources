# Glyphs Resources
A collection of resources for Glyphs App

## Hacks (This needs a better name)
### Hide Metrics in Text View
When the text tool is selected, the side-bearing values are visible beneath each character. By default, these metrics are hidden when the text is viewed at 75pt or smaller. To hide them at larger sizes, run the code below in the Macro panel. In this example, the metrics will be hidden at any size under 151pt.

`Glyphs.intDefaults["TextModeNumbersThreshold"] = 151`

