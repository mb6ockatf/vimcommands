# vimcommands

A brief reference for all necessary VIM editor commands.

> Usually, one-letter upper command means the same as lower one, but goes without taking punctuation into account. For instance, `cw` is for changing one word, and `cW` is the same but not counting punctuation. Or, the other case, to work at beginning of line, not at the current position.
> 
Also, double-letter command (i.e. `cc`, `dd`, `yy`) to affect the whole line.

- `vim <filename>` - open file
- `vim +*n* <filename>` - open file at line *n*
- `vim +/pattern <filename>` - open file at the first occurence of *pattern*
- `view <filename>` - view file in read-only mode. Same as `vim -R <filename>`
- `vi -r` or `ex -r` - a list of any files that the system has saved
- `vim -r <filename>` - recover file (in case system crashed while editing)
- `:w` to overwrite the source file with the current buffer.
- It is possible to specify the range of lines to be saved in as a new file: `:11,180w filename`
- `:r filename` to read a specified file into a current file. Synonim for `:read`.
- `:args` - to see all arguements vim was launched with
- `CTRL ^` - to move edit the other file specified in args


## Move
- `h` - moving left
- `l` - moving right
- `j` - moving down
- `k` - moving up
Scrolling screens:
- `CTRL F` - forward
- `CTRL B` - backward 
Scrolling half-screens:
- `CTRL D` - down (forward)
- `CTRL U` - up (backward)
- `+` - move to the first character of **next** line
- `-` - move to the first character of **previous** line
- `e`, `E` - move to the end of the word
- `w`, `W` - move forward one word
- `b`, `B` - move backward one word
- `$` - end of line
- `0` - beginning of line
- `z ENTER` - move cursor to the to the beginning of line and move the screen down til the line is the first to appear
- `z.` - move the line to the center of screen and scroll
- `z-` - move current line to bottom of screen and scroll
- `H` - move to `h`ome - the top line
- `M` - move to middle line
- `L` - move to last line
- *n*`H` - move *n* lines below top line
- *n*`L` - move to *n* lines above last line
- `^` - move to first nonblank character of the current line
- *n*`|` - move to column *n* of the current line
- `(` or `)` - move to beginning of current sentence or next sentence
- `{` or `}` - move to beginnig of current parapraph or next parapraph
- `[[` or `]]` - move to beginning of current section or next section 


## Editing

### Deletion
- `x` - one character. But `5x` is for five ones.
- `d` - actually, *d*elete
- `c` - change
- `S` - delete line and substitute text
- `R` - overstrilke existing characters with new text
- `u` - undo last change
- `U` - return to original state

### Adding text
- `i` - insert text at the current position
- `I` - insert text at the beginnig of line
- `a` - append text at the current position
- `A` - append text at the beginnig of line
- `o` - open new line below cursor for new text
- `O` - open new line above cursor for new text
- `J` - join current and next line (never mix it with lower `j`)

### Other
- `~` - toggle case
- `.` - repeat last action
- `P`, `p` - place text from buffer
- `ZZ` - save edits and quit file. (`w`rite command saves the whole file, although `ZZ` affects edits only. It is useful to use ZZ when editing large files.)
- `CTRL L` - redraw the screen
- `CTRL G` - shows some info (in case you're lost in a file)
- \`\` (two backquotes) - return to place where you started your search or place from where you moved with `G` command
- *n*`G` - goto *n* line of file. After this commang you can return to where you were with \`\` command

### Search
- `/` - search
- `n` - repeat search in same direction
- `N` - repeat search in opposite direction
- `/ ENTER` - repeat search forward
- `? ENTER` - repeat search backword
- `:set nowrapscan` - read more on the Internet
- `f`*x* - find the next occurence of *x* on the line
- `F`*x* - find the previous occurence of *x* on the line
- `t`*x* - move cursor to before the next occurence of *x* on the line
- `T`*x* - move cursor to after previous occurence of *x* on the line
- `;` - repeat previous find command the same direction
- `,` - repeat previous find command the opposite direction
- `:g/pattern` - an `ex` editor global search command. `:g/pattern/p` - to show all occurences
- Use `:g!` (with '!' mark) to show all lines not including the pattern
- You can specify a range of lines `:g` will search in: `:12,18g/pattern/p`


###
- `"` - making use of buffers
- `m`*x* - mark position with any letter (better to use lowercase)
- `'`*x* - move cursor to a line marked as *x*
- *x* - move cursor to a character marked by *x*

