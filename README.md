A jQuery on-screen keyboard (OSK) plugin that works in the browser. Originally posted by Jeremy Satterfield in his [blog](http://jsatt.blogspot.com/2010/01/on-screen-keyboard-widget-using-jquery.html), [jQuery plugins](http://plugins.jquery.com/project/virtual_keyboard) and on [Snipplr](http://snipplr.com/view/21577/virtual-keyboard-widget/). Currently maintained by [Mottie](https://github.com/Mottie/Keyboard).

[![Bower Version][bower-image]][bower-url] [![NPM Version][npm-image]][npm-url] [![devDependency Status][david-dev-image]][david-dev-url] [![Join the chat at https://gitter.im/Mottie/Keyboard][gitter-image]][gitter]

## Features ([Demo](http://mottie.github.com/Keyboard/))

### Ease of use

* An on-screen virtual keyboard embedded within the browser window which will popup when a specified entry field is focused.
* The user can then type and preview their input before Accepting or Canceling.
* It can be set to always remain open, and to not use a preview.

### Ease of installation

* Grab the files as a zip, or from npm or bower - see the [installation](#installation) section below.
* In a minimal setup, the keyboard works by including:
  * jQuery
  * jQuery UI theme
  * (optional) jQuery UI position utility to position the keyboard at the input/textarea element
  * Initialize keyboard - no options needed for qwerty keyboard.

### Ease of setup

* Add custom keyboard layouts easily.
* Multiple region specific keyboard layouts included in a separate directory. This is a work in progress and slowly growing.
* Add up to four standard key sets to each layout that use the shift and alt keys (default, shift, alt and alt-shift).
* Add any number of optional modifier keys (meta keys) to add more key sets.
* Each meta key set can also include the shift, alt and alt-shift keysets.
* Position the keyboard in any location around the element, or target another element on the page (using jQuery UI position utility).
* Easily modify the key text to any language or symbol.
* Allow direct input or lock the preview window.
* Set a maximum length to the inputted content.
* Scroll through the other key sets using the mouse wheel while hovering over a key to bypass the need to use alt, shift or meta keys.
* Easily type in characters with diacritics. Here are some default combination examples:
    * `'` + vowel ( vowel with acute accent, e.g. `'` + `e` = `é` )
    * `` ` `` + vowel ( vowel with grave accent, e.g., `` ` `` + `e` = `è` )
    * `"` + vowel ( vowel with diaeresis, e.g., `"` + `e` = `ë` )
    * `^` + vowel ( vowel with circumflex accent, e.g., `^` + `e` = `ê` )
    * `~` + certain letters ( letter with tilde, e.g. `~` + `n` = `ñ`, `~` + `o` = `õ` )
* Enable, disable or add more diacritic functionality as desired.
* Use callbacks and event triggers that occur when the keyboard is open or closed and when the content has changed, been accepted or canceled.
* Includes ARIA support (may not be fully implemented).
* Built in watermarking. It emulates HTML5's placeholder, if the browser doesn't support it.
* Include validation using a callback function so third-party validation methods can be used.

### Themes

* jQuery UI themes are used by default.
* Bootstrap themes ([original](http://jsfiddle.net/Mottie/MK947/1837/) or [dark](http://jsfiddle.net/Mottie/egb3a1sk/494/)) can also be applied.
* Or add a completely custom theme (without using jQuery UI position utility):
  * [Light](http://jsfiddle.net/Mottie/jsh0377k/) using [keyboard-basic.css](https://github.com/Mottie/Keyboard/blob/master/css/keyboard-basic.css).
  * [Dark](http://jsfiddle.net/Mottie/6dmqhLvh/) using [keyboard-dark.css](https://github.com/Mottie/Keyboard/blob/master/css/keyboard-dark.css).

### Extensions

* Alt-keys: Show alternate keys in a popup after long-clicking on a key.
* Autocomplete: Integrate with jQuery UI's autocomplete widget.
* Caret: Add a caret with custom styling.
* Extender: Add a togglable layout (e.g. toggle number pad)
* Keyset: Show shift, alt or meta keyset within the virtual keyboard - custom styling.
* Mobile: Use with jQuery Mobile.
* Navigate: Use arrow, home, end &amp; page up/down to navigate inside of the keyboard.
* Scramble: Scramble the entire keyset or by row, once or every time the keyboard is opened for added security.
* Typing: Allows you to simulate typing into the keyboard for demo purposes or to assist user input.

## Dependencies

* Required
    * jQuery 1.4.3+
    * jQuery caret (included with source)
* Optional
    * jQuery UI Positioning Utility (optional, if you position the keyboard yourself)
    * jQuery UI CSS (can be customized) / Bootstrap CSS
    * jQuery mousewheel plugin - allows using mousewheel to scroll through other key sets
    * jQuery UI Autocomplete widget - use with jQuery keyboard autocomplete extension

## Installation

* Download a [zip](https://github.com/Mottie/Keyboard/archive/master.zip) or [tar.gz](https://github.com/Mottie/Keyboard/archive/master.tar.gz) with all files, for use in the browser.
* Install using [bower](https://github.com/bower/bower) via `bower install keyboard`.
* Install using [npm](https://www.npmjs.com/) via `npm install virtual-keyboard`.
* [Use with AngularJs](https://github.com/antonio-spinelli/ng-virtual-keyboard) via `bower install ng-virtual-keyboard`.

## Documentation

Wiki: [Home](https://github.com/Mottie/Keyboard/wiki/Home) | [FAQ](https://github.com/Mottie/Keyboard/wiki/FAQ) | [Setup](https://github.com/Mottie/Keyboard/wiki/Setup) | [Usage](https://github.com/Mottie/Keyboard/wiki/Usage) | [Options](https://github.com/Mottie/Keyboard/wiki/Options) ( [Layout](https://github.com/Mottie/Keyboard/wiki/Layout), [Language](https://github.com/Mottie/Keyboard/wiki/Language), [Useability](https://github.com/Mottie/Keyboard/wiki/Useability), [Actions](https://github.com/Mottie/Keyboard/wiki/Actions) ) | [Methods](https://github.com/Mottie/Keyboard/wiki/Methods) | [Theme](https://github.com/Mottie/Keyboard/wiki/Theme) | [Log](https://github.com/Mottie/Keyboard/wiki/Log)

## To Do

* Waiting for requests :)
* Add more regional keyboard layouts.
* Add an input mask extension. I think I'll try to make it compatible with [this plugin](https://github.com/RobinHerbots/jquery.inputmask).
* Allow attaching a keyboard to a contenteditable element.

## Known Problems

* This plugin currently supports input and textarea elements. It does not yet support content editable elements.
* *Mobile*: If the key press lags behind by one character, it is likely due to the mousewheel plugin. Disable it. See issues [#379](https://github.com/Mottie/Keyboard/issues/379) &amp; [#411](https://github.com/Mottie/Keyboard/issues/411).
* *IE* and *Opera*:
    * In a text area with multiple carriage returns, the caret positioning will be off when repositioning it with the mouse.
    * Using the right and left arrow keys to navigate through a text area with multiple carriage returns is problematic. The caret doesn't behave like in other browsers when moving from one line to the next. You can always reposition the caret using the mouse.
* *Opera*: When pressing the tab key while inside a textarea, all browsers but Opera add the tab to the virtual keyboard textarea.
* *Safari*: See the QWERTY Text Area demo with a locked input. While using the virtual keyboard to type, it enters the text in backwards! This is because textareas with a "readonly" attribute always returns zero for the caret postion.
* *Typing Extension*:
    * When pressing "Alt", the key set will change to the alt key set, but the focus will be moved to the browser menu. Pressing it quickly a second time will return the focus. This is built into the browser and it isn't possible (as far as I know) to automatically restore the window focus the first time alt is pressed.
    * Holding down the Alt key and trying to type is also not possible since the Windows OS is assuming you are trying to type a shortcut key to access the browser menu. You can still click the keys in the alt key set with the mouse.
    * Simulated typing on the keyboard breaks when the CapLock is on. Still looking for a cross-browser solution.

## Contributing

* Install [node.js](http://nodejs.org/) - this includes `npm` (node package manager).
* Run `npm install` in the root directory.
* Run `npm install -g grunt-cli` to install the grunt command-line interface.
* Make any changes to the code.
* Unit tests will be added later.
* Run `grunt` to perform a new build in the `/dist` folder.
* Submit a pull request from a branch other than the `main`.

## Licensing

* Keyboard code: [MIT License](http://www.opensource.org/licenses/mit-license.php) for all versions.
* Caret code by C. F., Wong (Cloudgen): [MIT License](http://www.opensource.org/licenses/mit-license.php)
* Layouts files: Most are under [WTFPL](http://sam.zoy.org/wtfpl/), unless the file itself specifies otherwise.

[npm-url]: https://npmjs.org/package/virtual-keyboard
[npm-image]: https://img.shields.io/npm/v/virtual-keyboard.svg
[david-dev-url]: https://david-dm.org/Mottie/keyboard#info=devDependencies
[david-dev-image]: https://david-dm.org/Mottie/keyboard/dev-status.svg
[bower-url]: http://bower.io/search/?q=keyboard
[bower-image]: https://img.shields.io/bower/v/keyboard.svg
[gitter-image]: https://badges.gitter.im/Join%20Chat.svg
[gitter]: https://gitter.im/Mottie/Keyboard?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge

## Change Log

Only the latest changes will be shown below, see the [wiki log](https://github.com/Mottie/Keyboard/wiki/Log) to view older versions.

### Version 1.26.16 (2/1/2016)

* Core:
  * Add `userClosed` option. See [issue #415](https://github.com/Mottie/Keyboard/issues/415).
  * Add remove keyboard function & prevent memory leaks.
  * Reformat code.
* Scramble: Scramble once with multiple always open keyboards. Fixes [issue #430](https://github.com/Mottie/Keyboard/issues/430).

### Version 1.26.15 (1/19/2016)

* Add npm autoupdate data for cdnjs & version bump.

### Version 1.26.14 (1/19/2016)

* Core:
 * Fix action key class names - bug introduced in last update.
 * Triggered change events now use a modified keyboard event.
 * The lock (caps lock) key now "sticks" properly.
 * Call validate with empty input. Fixes [issue #429](https://github.com/Mottie/Keyboard/issues/429).
* Build: update dependencies.

### Version 1.25.13 (1/16/2016)

* Docs:
  * Update jQuery &amp; migrate plugin.
  * Add jQuery v3.0.0-beta1 to test.
* Core:
  * Fix ":" mapping & change key data-action values. Fixes [issue #425](https://github.com/Mottie/Keyboard/issues/425).
  * Dash &amp; underscore keys get a class name assigned.
* Typing:
  * Include arrow & other keys.
  * Fix issue where "." was not highlighted while typing.

### Version 1.25.12 (1/10/2016)

* Core:
  * Tweak capslock detection code. See [issue #416](https://github.com/Mottie/Keyboard/issues/416).
  * `restrictInput` matches accepted keys instead of replacing. Fixes [issue #419](https://github.com/Mottie/Keyboard/issues/419).
  * Fixed mapped &amp; accepted keys.
  * Add `last.preVal` which stores the previous value.
* AltKeysPopup:
  * Fix javascript error.
  * Prevent javascript error if altKey is undefined.
  * Tweak capslock detection code.
  * Prevent opening multiple popups.
  * Fix key highlighting on keyboard navigation.
  * Ensure all popup windows removed.
  * See [issue #416](https://github.com/Mottie/Keyboard/issues/416).
* Typing: Fix mapped key highlighting while typing.
* Build: Include unminified keyboard file in dist folder. See [issue #422](https://github.com/Mottie/Keyboard/issues/422).
