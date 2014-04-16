Salcode Vim Settings
====================
This is my attempt to move all my Vim settings into version control.

Setup
-----
The settings files: vimrc.config and gvimrc.config contain the
settings for .vimrc and .gvimrc respectively.

Rather than moving and renaming the files I recommend creating
links to them with the following line from the command line.

`ln -sf ~/salcode-vim-settings/vimrc.config ~/.vimrc && ln -sf ~/salcode-vim-settings/gvimrc.config ~/.gvimrc && ln -sf ~/salcode-vim-settings/vim ~/.vim`

### What this install line does
**ln -sf ~/salcode-vim-settings/vimrc.config ~/.vimrc**
makes .vimrc a link that points to the project's vimrc.config

**ln -sf ~/salcode-vim-settings/gvimrc.config ~/.gvimrc**
makes .gvimrc a link that points to the project's gvimrc.config

**ln -sf ~/salcode-vim-settings/vim ~/.vim**
makes .vim a link that points to the directory /vim in this project

### Link Notes:
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

### [Commentary](https://github.com/tpope/vim-commentary)
`gc` on visual selection commments selection (or uncomments)
`gcc` comments current line or uncomments
default comments are `/* */`, vimrc changes to `//` for php and js

### [Vim Markdown](https://github.com/plasticboy/vim-markdown)
Adds Markdown Syntax Highlighting

Author
------
Sal Ferrarello
http://twitter.com/salcode

Contributing
------------
Please make all Pull Requests against the `develop` branch
