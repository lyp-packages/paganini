# Paganini: A font package for lilypond

<p align="center">
  <a href="./example.ly">
  <img
    src="https://raw.githubusercontent.com/lyp-packages/paganini/master/example.png">
  </a>
</p>

This package provides the Paganini font for lilypond, created by [Abraham Lee](https://github.com/tisimst), found in  [OpenLilypondFonts](https://github.com/OpenLilypondFonts) and repackaged for usage as a lyp package@.

## Installation

Install using [lyp](https://github.com/noteflakes/lyp):

```bash
$ lyp install paganini
```

## Usage

```lilypond
\require "paganini"

% Use paganini font and apply associated stylesheet
\usePaganiniStyleSheet

% To use font only:
#(set-global-staff-size 16)  % this MUST go PRIOR to defining the fonts!!!
\paper {
  #(define fonts
    (set-global-fonts
      #:music "paganini"
      #:brace "paganini"
      #:factor (/ staff-height pt 20)
  ))
}
```

Also see the included [example](./example.ly).

## Compatibility with Lilypond versions

This font is known to work in Lilypond version 2.18.2 or later.

FONTLOG for the Paganini font
-----------------------------

This file provides detailed information on the Paganini Font Software. This information should
be distributed along with the Paganini fonts and any derivative works.


Basic font information
----------------------

Paganini is an OFL-licensed font based on the OFL-licensed Parnassus font by Kristof
Bastiaensen. Since Parnassus was designed for use with Musescore (notation software), a
remapping was necessary to make it compatible with LilyPond. OFL requires a name change in this
instance. This font software is not designed for use in a word-processing application, although
all the glyphs may be accessed at their respective Unicode points. It was originally designed
for use with LilyPond, the automatic music engraver.

More information about Parnassus can be found at:

http://www.resonata.be/archives/117

More information about LilyPond can be found at:

http://www.lilypond.org/

Changelog
---------

16 July 2013 (Kristof Bastiaensen) Parnassus version 1.0
- Initial design with basic set of classical notation glyphs.

30 July 2014 (Abraham Lee) Paganini version 1.0
- Initial design to be compatible with LilyPond 2.18.2. Renamed to Paganini
  to comply with OFL license terms.

30 September 2014 (Abraham Lee) Paganini version 1.0
- Added WOFF font file support
