---
Title: Atom keymap for translitering Arabic
Author: Jacob Høigilt
Date: August 2022
---
# Description and usage
This Markdown file contains code that you can put directly into your init.coffee and keymap.cson files in your Atom directory. Doing so will give you the keyboard shortcuts to transliterate Arabic (according to the Anglo-American standard of the *International Journal of Middle East Studies*). Restart Atom after you have made the changes.

Atom's own documentation for tinkering with these configuration files is here: https://flight-manual.atom.io/using-atom/sections/basic-customization/.

Changing the mapping and inserting different and/or additional shortcuts for alternative transliteration characters (such as /š/) is easy: just copypaste the code and insert the desired keystroke/character, for example from the Unicode library at https://www.unicode.org/charts/.

Below are, first, the code for the keymap.cson file, and second, the code for the init.coffee file (both including the default explanatory information in the files provided by the Atom team).
