# Notes for some command tools
## vim
This note is for **buffer**, **window**, **tab**, This note is based on [this blog](https://sanctum.geek.nz/arabesque/buffers-windows-tabs/)

#### buffer
* `:ls`: a quick list of the buffers open in a Vim session

#### window
A window in Vim is a viewport onto a single buffer. When you open a new window with `:split` or `:vsplit`, you can include a filename in the call. This opens the file in a new buffer, and then opens a new window as a view onto it. A buffer can be viewed in multiple windows within a single Vim session; you could have a hundred windows editing the same buffer if you wanted to.
* `ctrl+b c`: **create** a window

#### tab
* `:tabn` and `:tabp`: flick back and forth between the tabs
* `:tabnew`: Open a new tab
* `:tabedit <filename>`: Edit the file with the provided name in a new tab
* `gt`: Go to next tab open
* `gT`: Go to previous tab
* `<Ctrl-w> T`: Break the current window out to a new tab

#### some other useful commands
* `zz`: Center the current line within the window
* `zt`: Bring the current line to the top of the window
* `zb`: Bring the current line to the bottom of the window
* `:new filename`: Open a new window above the current window
* `:vnew filename`: Open a new window beside the current window
* `:split filename`: Edit the specified file in new window above the current window
* `:vsplit filename`: Edit the specified file in a new window beside the current window
