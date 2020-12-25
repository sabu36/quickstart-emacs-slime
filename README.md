## Basic emacs commands

On my computer:
* C = Ctrl
* M (meta) = Alt

Maybe try the commands on an existing file.

description | emacs command | mnemonic | vim command
---|---|---|---
undo | C-_ | | u
abort any command | C-g |
save | C-x-s | | :w
shell command | M-! | | :!
**movement** |
move vertically (across newline) | C-b, C-f | "b"ackward, "f"orward | 
move by word | M-b, M-f | | b, w
move horizontally | C-p, C-n | "p"revious, "n"ext
end of line | C-a, C-e | | 0, $
move by expression | C-M-b, C-M-f |
move by function | C-M-a, C-M-e |
line# | M-g-g \<number> | | \<number>gg
**editing** |
cut line | M-Sft-Bsp | | dd
cut word | M-Bsp, M-d | | db, dw
cut to end | C-k | | d$
start selection | C-Spc (or C-@) | | v
reindent selection | C-x Tab | | >>, <<
cut selection | C-w | | d
copy selection | M-w | | y
paste | C-y | "y"ank back | p
insert newline | C-M-o, C-o | "o"pen | O, o 
**search** |
search and move | C-r, C-s | | / ⇒ N, n
search and replace (to end of file) | M-% (or Esc-%) | | :%s/\<srch>/\<rpl>/gc
replace | , |
next | Bsp |
**multiple windows** |
split side by side | C-x 3 | | :vsp
switch | C-x o | "o"ther | C-w-w
close | C-x 0 | | :q

## Slime (plugin for Common Lisp)

To install on linux:\
`sudo apt-get install slime cl-swank`

To make slime [use](https://trac.clozure.com/ccl/wiki/InstallingSlime) Clozure, in ccl:
```
? (load "path/to/ergolib/init")  ; enable quicklisp 
…
? (require :ql)
…
? (ql:quickload :quicklisp-slime-helper)
```
then follow the instruction at the end of output.

To enter slime in emacs: M-x slime

To send a function from editor to repl: C-c-c

To see function definition from repl: M-. (called meta-point)\
To go back: M-,
