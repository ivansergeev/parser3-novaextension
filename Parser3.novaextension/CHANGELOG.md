## Version 0.5.5

Added: 
- Support slashes in methods and variables, such as `@/foo/bar[attr]` or `^/foo/bar[$attr]`

Fix:
- Copyright Clips (thanks Andrey Shpigunov)

## Version 0.5.4

Added:
- Completion for the SQL `BINARY`, `INET_ATON`, `INET6_ATON`, `INET_NTOA`, `INET6_NTOA`, `IGNORE`

## Version 0.5.3

Added:
- Special charsets: `^#0A`, `^#09`
- Now the `sql` methods with description and variations: single-line, multi-line, multi-line w/options

Fix:
- SQL-autocomplete

## Version 0.5.2

Added:
- `clean` transformation type

Fix:
- `^taint[transformation type;string]`

## Version 0.5

Support for the new version of Parser 3.4.6

Added:
- Configuration variables: `$CHARSETS`, `$LOCALS`, `$STRICT-VARS`, `$HTTPD`, `$cfg`
- Descriptions: foreach (hash), list (file), sql (table)
- Completions string.base64, file.base64 options: `$.pad()`, `$.url-safe()`, `$.wrap()`
- Completions: instance property description
- New features of math:convert
- HTTPD methods: `@config[cfg]` and `@preprocess[]`
- `^math:uuid[]` with options
- `^image::measure[]` options
- file:list options: `$.filter[]`, `$.stat[]`
- `^memory:auto-compact()`
- `^table.rename[]`
- curl option: `$.http_version[val]`
- file copy options: $.append(true)
- `locals` — method property, 'piece' — table attribute after splitting a string
- `^hash.select[]`,` ^hash.reverse[]`
- `^date::today(shift in days)` and description of constructors
- `^use[]` with options

Fix:
- Instance method name with numbers


## Version 0.4.14

Added:

- Few completions description (void:sql)
- LAST_INSERT_ID (SQL)

## Version 0.4.13

Added:

- Clips: the copyright header. Just type `copyright` and press Enter. Supported syntaxes: Parser 3, HTML, XML, CSS, JS, SASS/SCSS, SQL.

## Version 0.4.12

Added:

- Basic compatibility with Nova 4

Fix:

- highlighting variables with `-`

## Version 0.4.11

Added:

- Escaping variables

Changed:

- Colouring of the arguments separator in the methods
- Numbers color

## Version 0.4.10

Added:

- `TODO`, `FIX` and `FIXME` in the single comments: display in the Symbol tree and highlighting in the code. Example of use:

```
	# TODO: Hello, world!
	# FIX: diseases and wars on this planet!
```

## Version 0.4.9

Added a donation button. Now you can support the development of the Parser 3 extension.

## Version 0.4.8

Added:

- Completion for the SQL `LIMIT`
- The `if` statement is divided into single-line and multi-line
- Highlighting Parser 3 charsets
- Added a description of Parser 3 theme color concept

Changed:

- Parser 3 theme

## Version 0.4.7

Changed:

- Parser 3 theme

Fix:

- Minor highlighting fixes

## Version 0.4.6

Added:

- Highlighting and completing variables in brackets, such as `${some}`
- Highlighting properties in brackets, such as `$.[Hello world][!]`
- Highlighting and completing user properties

Fix:

- Highlighting variables starting with numbers
- Completion doesn't offer user methods in fields (after the dot)

## Version 0.4.5

Added:

- Fields `$SQL.connect-string`, `$request:charset`

Changed:

- Parser 3 theme

Fix:

- Violation of the theme when the text is adjacent to the closing bracket
- Color violation in code blocks `[]`

## Version 0.4.4

Added:

- Highlighting and completing user defined classes
- Static fields `$response:location` and `$response:refresh`

Changed:

- Disabled highlighting regex string

## Version 0.4.3

Added:

- Highlighting regex string with comments to parts of expressions (complex expressions may not be highlighted correctly)

Changed:

- Parser 3 theme (brackets, regex string)
- duplicate variables are available again (the chicken and egg problem)

Fix:

- Auto-completion `^regex::create[]`

## Version 0.4.2

Added:

- Comments to parts of expressions

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

- Variables `$result`,`$exception`,`$key`, `$value`, `$CLASS_PATH`, `$LIMITS`, `$MAIN`, `$MAIL`, `$MIME-TYPES` and `$SQL` no longer duplicated in auto-completion

## Version 0.4.1

Added:

- Highlighting and completing logical operators, boolean values, exceptions types and class types for logical conditions only
- `$result` and `$exception` variable
- `$exception` fields (type, source etc.)
- Highlighting properties for exception, hash, image, status
- SQL completing only at the first level in the sql block (like `^void:sql{...}`). Nested blocks (if, switch etc.) will only highlight SQL operators.

Changed:

- Parser 3 theme

## Version 0.4

Switching to deeper work with Parser 3 blocks.

Added:

- Highlighting and completing the transformation type for the tainted context only

  ```
  ^apply-taint[transformation type][...]
  ^taint[transformation type][...]
  ^untaint[transformation type]{...}
  ```

Fix:

- Highlighting `apply-taint`, `taint` and `untaint`

## Version 0.3.9

Added:

- All supported curl options
- HTML and CSS support (experimental feature)

Changed:

- Parser 3 theme

## Version 0.3.8

Changed:

- Multiline comment `^rem{...}` by default (⌘+/). Unfortunately, a single-line comment `#` doesn't work by keyboard shortcut.
- Parser 3 theme

Added:

- Few curl options
- Few sql keywords
- Highlighting class types

## Version 0.3.7

Added:

- Parser 3 theme (initial release)

Fix:

- Version 0.3.6 doesn't work correctly

## Version 0.3.6

Added:

- SQL support

## Version 0.3.5

Added:

- Xnode
- Few xdoc options
- Xdoc constants

## Version 0.3.4

Added:

- Few options
- Options description

## Version 0.3.3

Added:

- User variables autocomplete

## Version 0.3.2

Added:

- User methods autocomplete with description (from the comments above)
- Xdoc methods and fields
- Instance methods and fields descriptions

## Version 0.3

Initial release. Basic language support.
