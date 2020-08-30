# Notes for some command tools
## note for pactical vim book
#### chapter 1
###### Don’t Repeat Yourself
* The dot command lets us repeat the last change.
* `A`->`$a`, `C`->`c$`, `s`->`cl`, `S`->`^c$`
#### chapter 2, Norml Mode
###### Compose Repeatable Changes
* `dbx`, `bdw`, `daw`: (`.==x`, `.==dw`, `.==daw`)
* `<C+a>`, `<C+x>`: perform addition and subtraction on numbers. When run without a count they increment by one, but if we prefix a number,then we can add or subtract by any whole number
* `10<C+a>`: modify it to read 15 if we positioned our cursor on a 5 character. (“add [count] to the numberat or after the cursor” )
###### Combine and Conquer
* Operator + Motion = Action: `d{motion}`, `dl`, `dap`,`daw`
* `c`, `d`, `y`: change, delete, yank
* `g~`, `gu`, `gU`: swap case, make lowercase, make uppercase
* `>`, `<`, `=`: shift right, shift left, auto indent
* `dd`, `yy`, `>>`, `gUU`: Vim’s grammar has just one more rule: when an operator command is invokedin duplicate, it acts upon the current line

#### chapter 3, Insert Mode
* `<C+h>`: delete back one character(backspace)
* `<C+w>`: delete back one word
* `<C+u>`: delete back to start of the line.(We can also use them in Vim’s command line as well as in the bash shell)
* `<C+[>`, `<ESC>`: switch to normal mode
* `<C+o>`: Switch to Insert Normal mode.(We can fire off a single command, after which we’ll be returned to Insert mode immediately.)
* `<C+o>zz`: allow us to read half a screen above and below the line we’re working on, then put us straight back into Insert Mode

#### chapter 4, Visual Mode
* `v`, `V`, `<C+v>`, `gv`: character-wise, line-wise, block-wise visual mode, reselect the lase visual block
* `o`: Go to other end of highlighted text, toggle the free end.
###### Repeat Line-Wise Visual Commands
* `Vj>.`: indent 2 lines 2 tabs


#### chapter 6, Manage Multiple Files
* `:ls`,`:bnext`, `:bn`, `:bp`, `:bfirst`, `:blast`: buffer cmd
* `%` symbol indicates which buffer is visible, `#` symbol indicates the alternate file. 
* `C+6` or `C+^` toggles between current and alternate file.
* `:bdelete 1 2 3`, `:1,4 bdelete`, `:5,10bd`: delete buffers

* `<C+w> s`, `<C+w> v`: split window into equal windows, the two resulting split windows will contain the same buffer 

#### chapter 7, Open Files and Save Them to Disk
* `:edit %<TAB>`: The `%` symbol is a shorthand for the filepath of the active buffer, Pressing the <Tab> key expands the filepath
* `:edit %:h<TAB>`: The `:h` modifier removes the filename while preserving the rest of the path, typing `%:h<Tab>` is expanded to the full path of the currentfile’s directory.

#### chapter 8, Navigate Inside Files with Motions
###### disply lines, real lines
* `gh,gj,gk,gl`: same to h,j,k,l. but in disply lines
* `g0`: to first character of display line
* `g^`: to first nonblank character of real line
* `g$`: to end of display line

* `w, e, b, ge`: ge means backward to end of previous word
* `f{char}`: forward to the next occurrence of {char}
* `f{char}`: backward to the previous occurrence of {char}
* `t{char}`: forward to the character before the next occurrence of {char}
* `t{char}`: backward to the character after the previous occurrence of {char}
* `;`: repeat the last character-search command
* `,`: reverse the last character-search command

* `i)`,`i}`, `i]`,`i>`, `i'`, `i"`, `i``, `it`: inside of `),},...,',",tag`
* `a)`,`a}`, `a]`,`a>`, `a'`, `a"`, `a``, `at`: around, a pair of `),},...,',",tag`
* `iw`, `is`, `ip`: similarily
* `%`: Jump to matching parenthesis
* `(`, `)`: Jump to start of previous/next sentence
* `{`, `}`: Jump to start of previous/next paragraph


* `m{a-zA-Z}`, `'m{a-zA-Z}`, ``m{a-zA-Z}`: first  non-whitespace  character, exact  position  where  a  mark  was  set
###### Automatic Marks
* ````: Position before the last jump within current file
* ``.`: Location of last change
* ``<`: Start of last visual selection
* ``>`: End of last visual selection
#### chapter 9, Navigate Between Files with Jumps
* `<C+o>`, `<C+i>`: jump back and forth to traverse jump list(`:jumps`), each separate window has its own jump list
* `g;`, `g,`: traverse backwardand forward through the change list
* `mM`, ``M`: run `mM` before invoking `:vimgrep`, then snap back with the ``M`


