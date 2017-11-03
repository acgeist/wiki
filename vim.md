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
---
##### References
[Append Output of an External Command](http://vim.wikia.com/wiki/Append_output_of_an_external_command)  

---
This page was last updated: Wed 01 Nov 2017 08:32:01 AM EDT 
