> **NOTICE:** This repository is looking for a new owner+maintainer as I want to dedicate my focus on maintaining [xplr](https://github.com/sayanarijit/xplr). Please [contact me](https://arijitbasu.in) in case you are interested.

# xplr.vim

This is a fork of [nnn.vim](https://github.com/mcchrish/nnn.vim) modified to work with
[xplr](https://github.com/sayanarijit/xplr).

### Setup

Vim Plug:

```vim
call plug#begin('~/.vim/plugged')
" ...
Plug 'sayanarijit/xplr.vim'
" ...
call plug#end()

let g:nnn#layout = { 'window': { 'width': 0.9, 'height': 0.9, 'highlight': 'Debug' } }
let g:nnn#action = {
      \ '<c-t>': 'tab split',
      \ '<c-x>': 'split',
      \ '<c-v>': 'vsplit' }
let g:nnn#replace_netrw = 1
```

packer.nvim:

```lua
require("packer").startup(function()
  -- ...
  use({
    "sayanarijit/xplr.vim",
    config = function()
      vim.cmd([[
        let g:nnn#layout = { 'window': { 'width': 0.9, 'height': 0.9, 'highlight': 'Debug' } }
        let g:nnn#action = {
              \ '<c-t>': 'tab split',
              \ '<c-x>': 'split',
              \ '<c-v>': 'vsplit' }
        let g:nnn#replace_netrw = 1
      ]])
    end,
  })
  -- ...
end)
```

### Examples

Git project root

```
command XplrProjectRoot :XplrPicker `git rev-parse --show-toplevel`

:XplrProjectRoot
```

Current file

```
:XplrPicker %:p
```

Current working directory

```
:XplrPicker
```

Root
```
:XplrPicker /
```
