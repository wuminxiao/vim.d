# My VIM configuration

1. It works fine on 64bit Lubuntu with VIM 7.4.
1. It should be OK for other Linux and VIM 7.+.

## Install & Upgrade

### Install

1. Install `vundle`

        git clone http://github.com/gmarik/vundle.git ~/.vim/bundle/vundle

1. Clone `vim.d`

        git clone https://github.com/feiyuw/vim.d.git ~/Workspace/vim.d

1. Create `~/.vimrc`

        ln -s ~/Workspace/vim.d/vimrc ~/.vimrc

1. Open `gvim`, execute `:BundleInstall`

1. Open `gvim` again, enjoy!


### Upgrade

1. Update vim.d

        cd ~/Workspace/vim.d
        git pull

1. Open `gvim`, execute `:BundleClean`

1. Open `gvim`, execute `:BundleUpdate`


## Plugins

| *plugin*                          |   *description*                                           |
| --------------------------------- | --------------------------------------------------------- |
| `gmarik/vundle`                   | vim scripts manager                                       |
| `Solarized`                       | color schema                                              |
| `ctrlp.vim`                       | similar with sublime `Ctrl+P`                             |
| `taglist.vim`                     | show outline of code                                      |
| `minibufexpl.vim`                 | buffer list on the top panel                              |
| `The-NERD-tree`                   | project like file browser                                 |
| `NERD_tree-Project`               | auto determine project root path                          |
| `The-NERD-Commenter`              | comment/uncomment your code easilly                       |
| `pyflakes.vim`                    | pyflakes support for python file                          |
| `UltiSnips`                       | code snipper support                                      |
| `carlobaldassi/ConqueTerm`        | execute command on vim panel                              |
| `Markdown`                        | markdown syntax support                                   |

## Shortcuts

1. `,e`

    open file

1. `,s`

    open file in split window

1. `,vs`

    open file in vertical split window

1. `<Ctrl-m>`

    comment/uncomment code

1. `<F4>`

    open tag list on the right panel

1. `<F12>`

    open project browser on the left panel

1. `<F10>`

    open bash on the below panel

1. `<Ctrl-Tab>`

    in `normal` mode, switch files in minibuffer; in `insert` mode, used to select code snippet

1. `<Ctrl-p>`

    in `insert` mode, used to open specified file quickly;
    see detail in `ctrlp.vim` plugin

1. `,;`

    auto complete

1. `,t`

    open new tab

1. `,n`

    go to next tab

1. `<Ctrl-j>`

    * in `insert` mode, this is used to complete the snippet
    * try to type `img<Ctrl-j>` when editing a .md file, see what will happen
    * try to type `<Ctrl-j>` when you want to jump to next edit path
    * try `<Ctrl-k>` to jump back

1. `,c`

    copy to system clipboard

1. `,v`

    paste from system clipboard


## Some Tips

### Edit file in column

1. in `normal` mode, `<Ctrl-v>` start to select column, `<Shift-v>` to select multiple lines
1. after select several columns, 
    * `I` used to add content before cursor column
    * `A` used to add content after cursor column
    * `r` used to modify content in cursor column

### Quick Move

1. `<Ctrl-o>` move to previous edit position
1. `<Ctrl-i>` move to forward edit position
1. `b` move to previous word, `w` move to next word
    * try `B` and `W`, and see what's the difference
1. `{` move to previous block, `}` move to next block
1. `0` move to start of the line, `$` move to end of the line
    * `^` move to first char of the line
1. `gg` move to the start of the file, `G` move to the end of the file

### Quick Edit

1. `u` undo, `<Ctrl-r>` redo
1. `.` report last step
1. `di'` delete content in `'`
1. `dt'` delete content from current position to `'`
1. `cw` modify the current word
1. `caw` modify the current word
1. `c0` modify from start to current position
1. `c$` modify from current position to end of this line
1. `R` update the content

### Macro

1. `qa` start to record macro `a`
1. execute some steps
1. `q` stop to record
1. `@a` execute the macro
1. `@@` execute the last executed macro


## Reference

1. [VIM Tips](http://www.rayninfo.co.uk/vimtips.html)
1. [VIM scripts](http://vim-scripts.org)
1. [ctrlp.vim introduction](http://zuyunfei.com/2013/08/26/vim-plugin-ctrlp/)
