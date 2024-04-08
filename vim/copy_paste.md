# Copy and paste into Vim
## Replace whole file via PuTTY / SSH
- Open text file with Vim
- Delete everything with `:%d`
- Copy text
- Insert everything with `Shift + Insert`
## Paste without strange formatting
- Open file with Vim
- Go into paste mode with `:set paste`, then `i` --> `INSERT (paste)`
- Paste as usual
- Disable paste mode with `:set nopaste`