# Notes for some command tools
# Notes
* [vim](#vim)
  * [edit files](#edit-files)
  * [buffer](#buffer)
  * [tab](#tab)
    * [Navigation](#Navigation)
    * [other operations](#other-operation)
  * [window](#window)
  * [some other useful commands](#some-other-useful-commands)
  * [search](#search)
  
## vim
This note is for **buffer**, **window**, **tab**, This note is based on [this blog](https://sanctum.geek.nz/arabesque/buffers-windows-tabs/) and [tab](http://vim.wikia.com/wiki/Using_tab_pages) and [buffer](http://vim.wikia.com/wiki/Easier_buffer_switching)


#### .vimrc
* First install [Vundle](https://github.com/VundleVim/Vundle.vim)
* copy `.vimrc`
* `:source ~/.vimrc` reload vimrc
#### edit files
* `vim file1.txt file2.txt`:
* `:e /path/file.txt`: edit two files
* `:read file2.txt`: read the content of another file to current file directly below the current cursor
* `:8read file2.txt`: the content of file2.txt being placed the line below the specified line 8
* `:read !ls -a | grep '^\.' | grep --invert-match '\.DS_Store\|\.$'`: read from shell command output
* `:new`, `:vnew`: horizontal, vertical split window
* `:enew`: no split
* `:tabnew`: a new tab
#### buffer
* `:ls`, `:files`, `: buffers`: a quick list of the buffers open in a Vim session
* `:ls!`: Unlisted buffers can be included
* `:b`, `:bu`, `:buf filename`, `:buffer 5`: abbreviated switch to another buffer, can be given either the name or the number of the buffer to edit. 
* `:bp`, `:bn`: previous buffer, next buffer
* `b5`, `5<C-^>` or `5<C-6>`: An alternative which can be used from normal mode, switch to 5.
* `bf`, `bl`, `bm`: first, last, next modified buffer
* `b#`: alternative buffer, toggle
#### tab
###### Navigation
* `gt`: Go to next tab
* `gT`: Go to previous tab
* `{i}gt`: go to tab in position i
* `:tabn` and `:tabp`: flick back and forth between the tabs
* `:tabfirst`: go to first tab
* `:tablast`: go to last tab
* `:tabs`: list all tabs including their displayed windows
* `:tabm 0`: move current tab to first
* `:tabm:` move current tab to last
* `:tabm {i}`: move current tab to position i+1
* `Ctrl-PgDn`: go to next tab(also in insert mode)
* `Ctrl-PgUp`: go to previous tab(also in insert mode)
###### other operation
* `:tabnew`: Open a new tab
* `:tabedit/:tabe <filename>`: Edit the file with the provided name in a new tab
* `<Ctrl-w> T`: Break the current window out to a new tab
* `:tabc` or `:tabclose` or `ctrl-w c`: close current tab
* `:tabclose i`: close i-th tab
* `:tabonly`: close all other tabs (show only the current tab)
* `:tab all`: show each buffer in a tab (up to 'tabpagemax' tabs)
* `:tab help`: open a new help window in its own tab page
* `:tab drop file`: open {file} in a new tab, or jump to a window/tab containing the file if there is one
* `:tab split`: copy the current window to a new tab of its own
* A command like `:sp myfile.txt` creates a new window in the current tab editing the specified file. That window can be moved to a new tab by pressing `Ctrl-W T`, and can be copied to a new tab with the command `:tab sp`(split the current window, but open the split in a new tab). 
#### window
A window in Vim is a viewport onto a single buffer. When you open a new window with `:split` or `:vsplit`, you can include a filename in the call. This opens the file in a new buffer, and then opens a new window as a view onto it. A buffer can be viewed in multiple windows within a single Vim session; you could have a hundred windows editing the same buffer if you wanted to.

#### some other useful commands
* `zz`: Center the current line within the window
* `zt`: Bring the current line to the top of the window
* `zb`: Bring the current line to the bottom of the window
* `:new filename`: Open a new window above the current window
* `:vnew filename`: Open a new window beside the current window
* `:split filename`: Edit the specified file in new window above the current window
* `:vsplit filename`: Edit the specified file in a new window beside the current window
#### search
refer to [usage](http://vim.wikia.com/wiki/Searching), [pattern](http://vim.wikia.com/wiki/Search_patterns), [vimregex](http://vimregex.com/) for more infomation
* `*`, `#`: search forward, backward


* [regx](#regx)
  * [grep](#grep)
  * [vimregx](#vimregx)
  * [shell](#shell)
#### grep [Click here for more](https://www.cnblogs.com/peida/archive/2012/12/17/2821195.html)
* `grep -in '[\.$]' filename`: line end with char '.'
* `grep -in 'g..d' filename.txt`: count, ignore case, line. good, gasd, begin with g, end with d, two chars.  '.' represents exactly one char.
* `grep -in  'go\+d' file.txt`: + means one or more. 
* `grep -in  'go*d' file.txt`: * means zero or more. 
* `grep -in  'go\?d' file.txt`: ? means zero or one.
* `grep -in  'go\{2,\}d' file.txt`: {} means times occurs. {} has special meaning in shell.
