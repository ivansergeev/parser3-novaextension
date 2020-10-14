## Version 0.4.1

Added:
* highlighting and completing logical operators, boolean values, exceptions types and class types for logical conditions only
* `$result` and `$exception` variable
* `$exception` fields (type, source etc.)
* highlighting properties for exception, hash, image, status
* SQL completing only at the first level in the sql block (like `^void:sql{...}`). Nested blocks (if, switch etc.) will only highlight SQL operators.

Changed:
* Parser 3 theme

## Version 0.4

Switching to deeper work with Parser 3 blocks.

Added:
* highlighting and completing the transformation type for the tainted context only

	`^apply-taint[transformation type][...]`
	
	`^taint[transformation type][...]`
	
	`^untaint[transformation type]{...}`

Fix:
* highlighting `apply-taint`, `taint` and `untaint`

## Version 0.3.9

Added:
* all supported curl options
* HTML and CSS support (experimental feature)

Changed:
* Parser 3 theme

## Version 0.3.8

Changed:
* Multiline comment `^rem{...}` by default (⌘+/). Unfortunately, a single-line comment `#` doesn't work by keyboard shortcut.
* Parser 3 theme

Added:
* few curl options
* few sql keywords
* highlighting class types

## Version 0.3.7

Added:
* Parser 3 theme (initial release)

Fix:
* version 0.3.6 doesn't work correctly

## Version 0.3.6

Added:
* SQL support

## Version 0.3.5

Added:
* xnode
* few xdoc options
* xdoc constants

## Version 0.3.4

Added:
* few options
* options description

## Version 0.3.3

Added:
* user variables autocomplete

## Version 0.3.2

Added:
* user methods autocomplete with description (from the comments above)
* xdoc methods and fields
* instance methods and fields descriptions

## Version 0.3

Initial release. Basic language support.
