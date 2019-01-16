# Notes for some command tools
## vim
This note is for **buffer**, **window**, **tab**, This note is based on [this blog](https://sanctum.geek.nz/arabesque/buffers-windows-tabs/)

#### buffer
* `:ls`: a quick list of the buffers open in a Vim session

#### window
A window in Vim is a viewport onto a single buffer. When you open a new window with `:split` or `:vsplit`, you can include a filename in the call. This opens the file in a new buffer, and then opens a new window as a view onto it. A buffer can be viewed in multiple windows within a single Vim session; you could have a hundred windows editing the same buffer if you wanted to.
* `ctrl+b c`: **create** a window

#### tab
*`:tabn` and `:tabp`: flick back and forth between the tabs
