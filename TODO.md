# TODO

3.  Smooth out hover animations for
  *	 Find buttons
  *	 Command Palette
  *	 tabs
  *	 sidebar
 
9. 	Progress Bar ? 
	```json		
	{
	    "class": "progress_bar_control",
	    "layer0.tint": [30, 30, 30],
	    "layer0.opacity": 1.0
	},
	{
	    "class": "progress_gauge_control",
	    "layer0.tint": [144, 144, 144],
	    "layer0.opacity": 1.0,
	    "content_margin": [0, 6]
	},
	```
10. **Sidebar Icons need work**
	* I managed to theme the folders too, with:

	```json
	// Sidebar folder closed
	{
	  "class": "icon_folder",
	  "layer0.texture": "User/Theme - Default/icons/folder.png",
	  "layer0.opacity": 1.0,
	  "content_margin": [8, 8]
	  },
	// Sidebar folder open
	{
	  "class": "icon_folder",
	  "parents": {
	  	"class": "tree_row", 
	  	"attributes": "expanded"
	  	},
	  "layer0.texture": "User/Theme - Default/icons/folder_open.png",
	},
	```
11. Icons .tmpreferences files to add more icons
	* *How can I target* `.erb` *files so I can add a icon too them ? I tried* `source.rails` *and* `text.html.rails` *but it's not working.*
		* If you want to add specific icons for specific file types you need to:
		1. add the respective `file_type_desired.png` and `file_type_desired@2x.png` (for retina) in `/package/Theme - Theme_Name/icons/` folder (if `Theme - Theme_Name` folder does not exist create it yourself).
		2. create a new `Icon (new file type here).tmPreference` file and put it in either `/package/user/` or `/package/Theme - Theme_Name/` folder.
		3. in the newly created "Icon (new file type here)" file insert the following:
		```xml
		<?xml version="1.0" encoding="UTF-8"?>
		<!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs /PropertyList-1.0.dtd">
		<plist version="1.0">
		<dict>
		    <key>scope</key>
		    <string>%right scope for file type here%</string>
		    <key>settings</key>
		    <dict>
		        <key>icon</key>
		        <string>file_type_%new file type here%</string>
		    </dict>
		</dict>
		</plist>
		```
	4. For the scope of ```.erb``` files, it should be ```html.body.ruby```, but you can find it both by:
	  5. looking in the color scheme or language definition files to see which scopes are used for highlight.
	  6. add ```{ "keys": "ctrl+alt+shift+o"], "command": "show_scope_name" }``` to you user's keybindings, create a new ```.erb``` fyle and trigger the command to display current scope in the bottom status bar.

### Icon Prefs
*  AI
*  Apache conf
*  ASP
*  CFC
*  CFM
*  CoffeeScript
*  Dart
*  Default
*  Ex
*  Fish
*  FSharp
*  handlebars
*  Haskell GS
*  Haskell HAS
*  Haskell LHS
*  Haxe
*  Jade
*  Julia
*  Liquid
*  List
*  LSL
*  Lua Luac
*  Markup
*  Mocha
*  **AUDIO**
*  Mustache
*  PDF
*  PERL
*  R
*  Ruby RBW
*  Rust
*  SCSS / SASS
*  sublime-settings
*  SLIM
*  Smiley
*  Source
*  Stata
*  STylus
*  Swift
*  SVG
*  ToDO
*  Twig
*  **Video**
*  Vue
*  XML
*  GULPFILE

source.sublime-settings keyword.other.name.sublime-settings
source.sublime-settings constant.language.boolean.jsongenericarrayelements
source.sublime-settings string.jsongenericarrayelements
source.sublime-settings constant.numeric.jsongenericarrayelements


source.json meta.structure.array.json meta.structure.dictionary.json string.quoted.double.json

source.json meta.structure.array.json meta.structure.dictionary.json meta.structure.dictionary.value.json string.quoted.double.json

source.json meta.structure.array.json meta.structure.dictionary.json meta.structure.dictionary.value.json meta.structure.array.json constant.numeric.json

source.json meta.structure.array.json meta.structure.dictionary.json meta.structure.dictionary.value.json punctuation.separator.dictionary.pair.json

------

source.json meta.structure.dictionary.json meta.structure.dictionary.value.json string.quoted.double.json

source.json meta.structure.dictionary.json meta.structure.dictionary.value.json meta.structure.array.json string.quoted.double.json