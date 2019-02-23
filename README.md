# Vim setup/configuration

The `.vimrc` setup is based on [https://github.com/amix/vimrc](https://github.com/amix/vimrc).

## Navigation

* switch windows: `ctrl-h`, `ctrl-l`, `ctrl-j`, `ctrl-k`
* next/previous buffer: `;l`, `;h`

## List of plugins:

### [vim-plug](https://github.com/junegunn/vim-plug)
Vim plugin manager. Use `:PlugInstall` inside vim to install all the plugins listed in `.vimrc`.

### [Goyo](https://github.com/junegunn/goyo.vim)
Writes vim with no distraction.

### [NERDTree](https://github.com/scrooloose/nerdtree)
Folder tree explorer, uses `ctrl-n` to toggle.
    
### [Ack](https://github.com/mileszs/ack.vim)
folder recursive Search.

For MacOS, need to install ack with
    ```
    brew install ack
    ```
For Ubuntu, need to install ack with
    ```
    apt-get install ack-grep
    ```

### grip
To preview markdown file in github style in terminal, installed with
    ```
    brew install grip
    ```

### [vim-markdown-preview](https://github.com/JamshedVesuna/vim-markdown-preview)

To fast preview mardown file from vim, hotkey: ctrl-p.

### [emmet-vim](https://github.com/mattn/emmet-vim)

The zen coding/emmet for vim, used <Tab> as the expanding key, used ctrl-y as expanding key.

### [ctrlp](https://github.com/ctrlpvim/ctrlp.vim)
Fast open file, much like cmd+p in visual studio code or sublime text, uses `ctrl-p`,

### [vim-commentary](https://github.com/tpope/vim-commentary)
Comment stuff out, uses `ctrl-i`.

### [vim-fugitive](https://github.com/tpope/vim-fugitive)
Git wrapper. 

    * `:Gdiff`
    * `:Gstatus`
    * `:Git ...`

### [ale](https://github.com/w0rp/ale)
Linter that supports multiple languages using [LSP](https://langserver.org/)(Language Server Protocol).

    * Typescript: one need to install typescript with `npm install -g typescript` for ale linter to work
    * Golang: one need to install go executable for ale linter to work



### [vim-go](https://github.com/fatih/vim-go)
Vim go plugins, some useful features:

    * `:GoDef/gd`: go to definition
    * `:GoImports`: import necessary packages
    * `GoInstall!`: go install command that shows all the errors if any
    * `:GoBuild`: go build command
> Note: completion is toggled by typing `ctrl-x ctrl-o`
> Note: before using any of the features, make sure the go executable is installed and run `:GoInstallBinaries` inside vim

### [typescript-vim](https://github.com/leafgarland/typescript-vim)
Typescript syntax highlight

### [tagbar](https://github.com/majutsushi/tagbar)
A plugin that shows class outlines and functions/variables of a file, type :TagbarToggle to toggle the window.
>Note: under ubuntu, remember to install exuberant-ctags with `apt install exuberant-ctags`.

### [vim-airline](https://github.com/vim-airline/vim-airline)
A plugin for statusline.

### [youcompleteme](https://github.com/valloric/youcompleteme)1
A plugin for autocompletion, check the website for installation guide

### [vim-flake8](https://github.com/nvie/vim-flake8)
A python lint plugin.
> Note: before using it, remember to install flake8 with pip globally:
`pip install flake8`

### [term](https://github.com/ternjs/tern_for_vim)
A javascript editting support plugin that allows go to definition, the most useful feature is `:TernDef`
