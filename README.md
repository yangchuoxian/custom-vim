# Vim setup/configuration

- [Vim setup/configuration](#vim-setupconfiguration)
  - [Navigation](#navigation)
  - [List of plugins:](#list-of-plugins)
    - [vim-plug](#vim-plug)
    - [Goyo](#goyo)
    - [NERDTree](#nerdtree)
    - [Ack](#ack)
    - [grip](#grip)
    - [vim-markdown-preview](#vim-markdown-preview)
    - [emmet-vim](#emmet-vim)
    - [ctrlp](#ctrlp)
    - [vim-commentary](#vim-commentary)
    - [vim-fugitive](#vim-fugitive)
    - [ale](#ale)
    - [vim-go](#vim-go)
    - [typescript-vim](#typescript-vim)
    - [tagbar](#tagbar)
    - [vim-airline](#vim-airline)
    - [youcompleteme1](#youcompleteme1)
    - [vim-flake8](#vim-flake8)
    - [term](#term)
    - [vim-prettier](#vim-prettier)
    - [dart-lang/dart-vim-plugin](#dart-langdart-vim-plugin)
    - [thosakwe/vim-flutter](#thosakwevim-flutter)
  - [Personal Settings](#personal-settings)
  - [Notes](#notes)
  - [knowledge](#knowledge)

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

To fast preview mardown file from vim, hotkey: ctrl-p

### [emmet-vim](https://github.com/mattn/emmet-vim)

The zen coding/emmet for vim, used <Tab> as the expanding key, used ctrl-y as expanding key.

### [ctrlp](https://github.com/ctrlpvim/ctrlp.vim)
Fast open file, much like cmd+p in visual studio code or sublime text, uses `ctrl-p`.


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


In order for Javascript "Jump to definition" to work, after installing ctags, put the `.ctags` file inside home folder, then under your javascript project folder, type

```shell
ctags -R .
```
It will generate a `tags` file, then inside VIM, type "Ctrl ]" to jump to definition.

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

### [vim-prettier](https://github.com/prettier/vim-prettier)
A javascript/scss/css plugin that allows auto-formatting based on config rules by typing <mapleader> + p

### [dart-lang/dart-vim-plugin](https://github.com/dart-lang/dart-vim-plugin)
Dart plugin

### [thosakwe/vim-flutter](https://github.com/thosakwe/vim-flutter)
Flutter plugin

## Personal Settings

* Under MacOS/Linux, allows Vim use system clipboard
* Enables code folding, use 'za', 'zo' 'zc'
* Disables ALE code auto completion
* For CtrlP, ignores `node_modules`, `DS_Store` and `git` folder/file
* To see recent search history: type 'q/'
* To see recent commands history: type 'q:'
* To go to previous command, type ':' then arrow key
* To paste yanked content into command area, type ':', 'C-r' then '"'

## Notes

Macro is a very useful ways to repeat action combinations:

* to start recording a macro, type `qq`
* to quit recording type `q`
* to repeat the macro, type `@q`

## knowledge

* `~` switches character case(uppercase to lowercase and vice versa)
* If you want to search something and have caret located at the end of the search place, type `/someThingToSearch/e`