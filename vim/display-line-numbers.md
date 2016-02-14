# Display Line Numbers

It is easy to show line numbers in vi (or **vim**).

You show line numbers by issuing the "set number" command:
`:set number`

or 

`:set nu`

If you want to turn off the line number display issue the "set nonumber" command:
`:set nonumber` 

or

`:set nonu`

or 

`:set nu!`

If you need line numbers every time you start vi/vim, append the following line to your `~/.vimrc` file:
`vim ~/.vimrc`

Append the following line:

`set number`

## NOTE
Issue these vim commands while in "command mode" of the vi/vim editor. Hit the [**Esc**] key to get into the command mode. Then type the : character at the beginning of the above commands.

### Reference

1. [link 1](http://alvinalexander.com/blog/post/linux-unix/how-display-line-numbers-vi-vim-editor)
2. [link 2](http://vim.wikia.com/wiki/Display_line_numbers)
3. [link 3](http://www.cyberciti.biz/faq/vi-show-line-numbers)
