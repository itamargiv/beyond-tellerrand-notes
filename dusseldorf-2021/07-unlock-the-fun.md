# Unlock The Fun!

By: Ulrike Rausch

- Creating handwritten fonts requires quite a lot of technical work.
- Actual handwritten sign looks much more charming than handwritten fonts.
- This is because letters that are computed look identical, and without the
  irregularities it makes it easy for us to detect pseudo handwriting.

## Open Type Features

- OTF allows us to have over 65k chars in a font file
- To give the impression of real handwritten text, you can have many different
  variations of the same letter
- A lot of the software we use has substitution mechanisms that choose
  variations for the users w/o them having to pick them manually
- There a called open type features. An example is the `fi` ligature
  substitution which
- We can program Open type features that will replace variations by context:
  "contextual alternates feature"
- Open Type features can be disable with css' `font-feature-settings` property.
  In order to turn features on an off you have to know their four letter feature
  codes.
- To get the available feature codes for each font you can use an online tools
  such as `fontdrop.com` or `wakamaifondue.com`

## Creating Handwritten fonts

- To create HW fonts, we scan text, and vector trace it - but that produces some
  unnatural results, all the shades and pressure points were lost.
- Color fonts came to the rescue, so instead of vector tracing them we create a
  bitmap or png and collect these scans into an open type font.
- Color fonts also support open type features: so we can include ligatures for
  natural writing flow, and contextual alternates for a more natural non
  repetitive look.
- Ligatures can also replace some emojis with ballpoint pen drawings, and each
  character pair can have alternate connecting strokes.
- Strike-through and underline can also utilize contextual alternates to have
  different effects

## More Fun with color fonts

- In a vectorized version of a handwritten font, we can control various
  [variable font axes](./02-VFWTF.md) such as wavelength, sloppiness etc.
- Color fonts also have support for vectorized layered fonts.
- Unfortunately with color fonts users cannot choose the font color
- We can use contextual alternates also to choose various color variations
  according to context
- We can even animate colors and gradients with clever usage of SVG and some
  experimental gusto.
- However we can combine variable fonts, which can be animated with css
  animations with color fonts to make the dream of animated fonts come to life!

## See more
- liebefonts.com: Ulrike's handwritten fonts
- typearture.com: Incredible experiments with variable color fonts, and css
  animations.