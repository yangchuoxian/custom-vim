# Vim setup/configuration

The `.vimrc` setup is based on [https://github.com/amix/vimrc](https://github.com/amix/vimrc).

## Navigation

* switch windows: `ctrl-h`, `ctrl-l`, `ctrl-j`, `ctrl-k`
* next/previous buffer: `;l`, `;h`

## List of plugins:

### [vim-plug](https://github.com/junegunn/vim-plug)
Vim plugin manager.

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

To fast preview mardown file from vim, hotkey: ctrl-p

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
Linter that supports multiple languages using [LSP](https://langserver.org/)(Language Server Protocol)

### [vim-go](https://github.com/fatih/vim-go)
Vim go plugins, some useful features:

    * `:GoDef/gd`: go to definition
    * `:GoImports`: import necessary packages
    * `GoInstall!`: go install command that shows all the errors if any
    * `:GoBuild`: go build command
> Note: completion is toggled by typing `ctrl-x ctrl-o`

### [typescript-vim](https://github.com/leafgarland/typescript-vim)
Typescript syntax highlight
