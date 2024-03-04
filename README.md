### LITE 1.0.0-alpha02 Release Notes ###

- New features:
	- New keyword: `until` will replace `while` when constructing `repeat` statements.
		- Old syntax: `repeat { ... } while(...)`
		- New syntax: `repeat { ... } until(...)`
	- New instructions:
		- Increment instruction: Increments a variable. Using it as an expression itself is not allowed, unlike in C.
			- Syntax: `myVar++`
		- Decrement instruction: Decrements a variable. Using it as an expression itself is not allowed, unlike in C.
			- Syntax: `myVar--`
	- New restrictions:
		- Function name declarations cannot begin with double underscore symbols (`__`)
		- Variable name declarations cannot begin with double underscore symbols (`__`)	
	- Quality of life:
		- Any `.lite` file gets `litestd` included by default. Including it manually results in a warning and is ignored.
		- Function name and variable name declarations may now also start with an underscore
- Bugfixes:
	- Windows: 
		- Fixed illegal memory access resulting in "Missing symbol WinMain@16"
		- Fixed syntax error if file does not end with a newline
		- Fixed `litec` unable to check latest version if called outside of %LITEPATH% directory
	- Global:
		- let (C equivalent of const) string variables printing memory address instead of text when calling `litestd` `print` / `println`
		

### Useful Links: ###

- BugTracker Trello board: https://trello.com/b/ldxnIZUj/lite-alpha-bugtracker
- VSCode extension: https://marketplace.visualstudio.com/items?itemName=LITE-Lang.lite-lang-alpha
	 