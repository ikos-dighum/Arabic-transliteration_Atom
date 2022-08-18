
Below are, first, the code for the keymap.cson file, and second, the code for the init.coffee file (both including the default explanatory information in the files provided by the Atom team).

## The keymap.cson file:
```
# Your keymap
#
# Atom keymaps work similarly to style sheets. Just as style sheets use
# selectors to apply styles to elements, Atom keymaps use selectors to associate
# keystrokes with events in specific contexts. Unlike style sheets however,
# each selector can only be declared once.
#
# You can create a new keybinding in this file by typing "key" and then hitting
# tab.
#
# Here's an example taken from Atom's built-in keymap:
#
# 'atom-text-editor':
#   'enter': 'editor:newline'
#
# 'atom-workspace':
#   'ctrl-shift-p': 'core:move-up'
#   'ctrl-p': 'core:move-down'
#
# You can find more information about keymaps in these guides:
# * http://flight-manual.atom.io/using-atom/sections/basic-customization/#customizing-keybindings
# * http://flight-manual.atom.io/behind-atom/sections/keymaps-in-depth/
#
# If you're having trouble with your keybindings not working, try the
# Keybinding Resolver: `Cmd+.` on macOS and `Ctrl+.` on other platforms. See the
# Debugging Guide for more information:
# * http://flight-manual.atom.io/hacking-atom/sections/debugging/#check-the-keybindings
#
# This file uses CoffeeScript Object Notation (CSON).
# If you are unfamiliar with CSON, you can read more about it in the
# Atom Flight Manual:
# http://flight-manual.atom.io/using-atom/sections/basic-customization/#configuring-with-cson
'atom-text-editor':
  'alt-a': 'custom:insert-longa'
  'alt-shift-a': 'custom:insert-caplonga'
  'alt-i': 'custom:insert-longi'
  'alt-shift-i': 'custom:insert-caplongi'
  'alt-u': 'custom:insert-longu'
  'alt-shift-u': 'custom:insert-caplongu'
  'alt-d': 'custom:insert-dad'
  'alt-shift-d': 'custom:insert-capdad'
  'alt-h': 'custom:insert-ha'
  'alt-shift-h': 'custom:insert-capha'
  'alt-s': 'custom:insert-sad'
  'alt-shift-s': 'custom:insert-capsad'
  'alt-t': 'custom:insert-ta'
  'alt-shift-t': 'custom:insert-capta'
  'alt-ø': 'custom:insert-ayn'
  'alt-æ': 'custom:insert-hamza'

```
## The init.coffee file:
```
# Your init script
#
# Atom will evaluate this file each time a new window is opened. It is run
# after packages are loaded/activated and after the previous editor state
# has been restored.
#
# An example hack to log to the console when each text editor is saved.
#
# atom.workspace.observeTextEditors (editor) ->
#   editor.onDidSave ->
#     console.log "Saved! #{editor.getPath()}"
# Keymapping

atom.commands.add 'atom-text-editor',
  'custom:insert-longa': (event) ->
    editor = @getModel()
    editor.insertText('ā')
  'custom:insert-longi': (event) ->
    editor = @getModel()
    editor.insertText('ī')
  'custom:insert-caplonga': (event) ->
    editor = @getModel()
    editor.insertText('Ā')
  'custom:insert-caplongi': (event) ->
    editor = @getModel()
    editor.insertText('Ī')
  'custom:insert-longu': (event) ->
    editor = @getModel()
    editor.insertText('ū')
  'custom:insert-caplongu': (event) ->
    editor = @getModel()
    editor.insertText('Ū')
  'custom:insert-dad': (event) ->
    editor = @getModel()
    editor.insertText('ḍ')
  'custom:insert-capdad': (event) ->
    editor = @getModel()
    editor.insertText('Ḍ')
  'custom:insert-ha': (event) ->
    editor = @getModel()
    editor.insertText('ḥ')
  'custom:insert-capha': (event) ->
    editor = @getModel()
    editor.insertText('Ḥ')
  'custom:insert-sad': (event) ->
    editor = @getModel()
    editor.insertText('ṣ')
  'custom:insert-capsad': (event) ->
    editor = @getModel()
    editor.insertText('Ṣ')
  'custom:insert-ta': (event) ->
    editor = @getModel()
    editor.insertText('ṭ')
  'custom:insert-capta': (event) ->
    editor = @getModel()
    editor.insertText('Ṭ')
  'custom:insert-ayn': (event) ->
    editor = @getModel()
    editor.insertText('ˁ')
  'custom:insert-hamza': (event) ->
    editor = @getModel()
    editor.insertText('ˀ')
```
