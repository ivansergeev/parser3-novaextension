## Version 0.4.8

Added:
* completion for the SQL `LIMIT`
* the `if` statement is divided into single-line and multi-line
* highlighting Parser charsets

## Version 0.4.7

Changed:
* Parser 3 theme

Fix:
* minor highlighting fixes

## Version 0.4.6

Added:
* highlighting and completing variables in brackets, such as `${some}`
* highlighting properties in brackets, such as `$.[Hello world][!]`
* highlighting and completing user properties

Fix:
* highlighting variables starting with numbers
* completion doesn't offer user methods in fields (after the dot)

## Version 0.4.5

Added:
* fields `$SQL.connect-string`, `$request:charset`

Changed:
* Parser 3 theme

Fix:
* violation of the theme when the text is adjacent to the closing bracket
* color violation in code blocks `[]`

## Version 0.4.4

Added:
* highlighting and completing user defined classes
* static fields `$response:location` and `$response:refresh`

Changed:
* disabled highlighting regex string

## Version 0.4.3

Added:
* highlighting regex string with comments to parts of expressions (complex expressions may not be highlighted correctly)

Changed:
* Parser 3 theme (brackets, regex string)
* duplicate variables are available again (the chicken and egg problem)

Fix:
* auto-completion `^regex::create[]`

## Version 0.4.2

Added:
* comments to parts of expressions

	```
	^if(
		def $fruit		# Do I have any fruit?
		&& $fruit eq banana	# Could it be a banana?
	){
		I have fruit!
	}
	
	^eval(
		3+2 # equal to 5
	)
	
	$abc(
		3*2 # equal to 6
	)
	```

Changed:
* variables `$result`,`$exception`,`$key`, `$value`, `$CLASS_PATH`, `$LIMITS`, `$MAIN`, `$MAIL`, `$MIME-TYPES` and `$SQL` no longer duplicated in auto-completion

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

	```
	^apply-taint[transformation type][...]
	^taint[transformation type][...]
	^untaint[transformation type]{...}
	```

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
