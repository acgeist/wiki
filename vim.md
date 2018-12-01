[Wiki Homepage](index.md)
# Vim 
### Random Tricks
* Read the output of a bash command  
 `:read !bashcommand <CR>`

* Copy/paste from one session to another
 
 In source file (start in normal mode):
 1. Use `ma` to mark first line
 2. Use `mb` to mark last line
 3. Use `:'a,'b w! xfer` to write out range to a scratch file
 
 In destination file:
 1. Move cursor to desired paste location
 2. Ensure you're in normal mode
 3. Use `:r xfer` to read in text

* Search and Replace Tricks
 1. Capture Groups: enclose portion between `\(` and `\)`, refer to it with `\1`, `\2`, etc. sequential.
 2. Visual Mode: `v`, select desired text, `:s` (will create a command that looks like `'<,'>s/find/replace with/flags`)
 3. Scope: `:s` refers to current line, `:5,9s` refers to lines 5-9 inclusive, `:%s` refers to entire file.  
 Examples:  
`'<,'>s/,\(\d\),/, \1,/g` looks for a comma followed by a single digit followed by another comma and inserts a space between the first comma and the digit.  Command will apply to a visual selection.

* Put Vim in the background and execute some terminal commands
`<Ctrl-z>`
Run terminal commands
`$ fg` to go back to Vim.

---
##### References
[Append Output of an External Command](http://vim.wikia.com/wiki/Append_output_of_an_external_command)  
[Vim Regex](http://www.vimregex.com)

---
This page was last updated: Sun 20 May 2018 10:46:50 PM EDT 

