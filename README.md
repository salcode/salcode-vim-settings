Salcode Vim Settings
====================
This is my attempt to move all my Vim settings into version control.

Setup
-----
The settings files: vimrc.config and gvimrc.config contain the
settings for .vimrc and .gvimrc respectively.

Rather than moving and renaming the files I recommend creating
links to them with the following line from the command line.

### Download
`git clone --recursive https://github.com/salcode/salcode-vim-settings.git ~/salcode-vim-settings`

### Configure/Install
`ln -sf ~/salcode-vim-settings/vimrc.config ~/.vimrc && ln -sf ~/salcode-vim-settings/gvimrc.config ~/.gvimrc && ln -sf ~/salcode-vim-settings/vim ~/.vim`

#### What this install line does
**ln -sf ~/salcode-vim-settings/vimrc.config ~/.vimrc**
makes .vimrc a link that points to the project's vimrc.config

**ln -sf ~/salcode-vim-settings/gvimrc.config ~/.gvimrc**
makes .gvimrc a link that points to the project's gvimrc.config

**ln -sf ~/salcode-vim-settings/vim ~/.vim**
makes .vim a link that points to the directory /vim in this project

#### Link Notes:
-f = if target already exists unlink and create new link  
-s = create a symbolic link

Default Configurations
----------------------
<leader> is mapped to `,`

Shortcuts
---------
`jk` is mapped to ESC in visual mode

`<leader>t2` change tab size to 2 spaces  
`<leader>t4` change tab size to 4 spaces

`<leader>w` clean all trailing whitespace

`<leader>el` the current expression on a line and error log it with comment  
**$str** becomes **error_log( '$str = ' . print_r( $str, true ) );**

`<leader>ev` edit .vimrc file  
`<leader>sv` source .vimrc file (i.e. apply settings in that file)

`<leader>eg` edit .gvimrc file  
`<leader>sg` source .gvimrc file (i.e. apply settings in that file)

Plugins
-------
Plugins are added as submodules, to update all submodules use
`git submodule update --init --recursive`

### [Pathogen](https://github.com/tpope/vim-pathogen)
Makes it easy to install plugins. Add the plugin project directory
to `vim/bundle` and pathogen manages things from there.  
**NOTE** to update documentation after installing a new plugin run `:Helptags`

### [NERDCommenter](https://github.com/scrooloose/nerdcommenter)
`<leader>c<space>` toggle comment state based on first line of selection
`<leader>cs` comment in sexy style
`<leader>cu` uncomment lines

### [Vim Markdown](https://github.com/plasticboy/vim-markdown)
Adds Markdown Syntax Highlighting

### [Syntastic](https://github.com/scrooloose/syntastic)
Syntax highlighting with errors notated with `>>` along the left side.

### [PDV](https://github.com/tobyS/pdv)
Create PHP Doc Blocks
`<leader>d` to trigger

### [Vmustache](https://github.com/tobyS/vmustache)
Dependency of PDV

### [NERDTree](https://github.com/scrooloose/nerdtree)
File browser bar on the side of your editor.
`<leader>nt` is mapped to open NERDTree
[Usevim Helpful NERDTree info](http://usevim.com/2012/07/18/nerdtree/)

`I`: Toggle hidden files  
`?`: Toggle NERD Tree's quick help  
`m`: Show the NERD Tree menu  
`t`: Open the selected file in a new tab  
`R`: Refresh the tree, useful if files change outside of Vim  
`i`: Open the selected file in a horizontal split window  
`s`: Open the selected file in a vertical split window  


Author
------
Sal Ferrarello
http://twitter.com/salcode

Contributing
------------
Please make all Pull Requests against the `develop` branch
