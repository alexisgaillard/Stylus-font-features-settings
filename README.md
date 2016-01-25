# Stylus position mixin
A Stylus mixin to manage the font-features-settings properties.

### Dependencies
  * [stylus](https://github.com/LearnBoost/stylus)

Example:
```stylus
@import "fontFeatureSettings"

body
  fontFeatureSetting(common-ligature discretionary-ligature historical-ligature proportional-number-spacing)

.Div__one
  fontFeatureSetting(superiors-positioning slashed-zero-extra)

.Div__three
  fontFeatureSetting(swash-alternative contextual-alternative historical-alternative set-1)
```

Will output:
```css
body {
  -moz-font-feature-settings: "liga" 1, "dlig" 1, "hlig" 1, "pnum" 1;
  -webkit-font-feature-settings: "liga" 1, "dlig" 1, "hlig" 1, "pnum" 1;
  font-feature-settings: "liga" 1, "dlig" 1, "hlig" 1, "pnum" 1;
}
.Div__one {
  -moz-font-feature-settings: "subs" 1, "zero" 1;
  -webkit-font-feature-settings: "subs" 1, "zero" 1;
  font-feature-settings: "subs" 1, "zero" 1;
}
.Div__three {
  -moz-font-feature-settings: "swsh" 1, "calt" 1, "hist" 1, "ss01" 1;
  -webkit-font-feature-settings: "swsh" 1, "calt" 1, "hist" 1, "ss01" 1;
  font-feature-settings: "swsh" 1, "calt" 1, "hist" 1, "ss01" 1;
}
```
Complete list of arguments:
- Ligature: common-ligature discretionary-ligature historical-ligature contextual-ligature
- Letter Case: small-caps small-caps-from-caps
- Number Case: lining-number-case or olstyle-number-case
- Number Spacing: proportional-number-spacing or tabular-number-spacing
- Fraction: normal-fraction or alternate-fraction
- Positioning: superiors-positioning inferiors-positioning
- Numeric Extras: slashed-zero-extra alternate-annotation-extra
- Character Alternatives: swash-alternative contextual-alternative historical-alternative stylistic-alternative
- Alternative Stylistic Set: set-1 set-2 set-3 set-4 set-5 set-6 set-7 set-8 set-9

Support:
 IE 9+, Edge 11+, Firefox 41+, Chrome 44+, Safari 9+, Opera 33+, IOS 9.2+, Android 4.3+, Chrome for Android 
## Credits

Developed by [Alexis Gaillard](https://alexisgaillard.com/). Licensed under [MIT](http://opensource.org/licenses/mit-license.php).
