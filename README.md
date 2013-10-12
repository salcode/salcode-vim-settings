Salcode Vim Settings
====================
This is my attempt to move all my Vim settings into version control.

Setup
-----
The settings files: vimrc.config and gvimrc.config contain the
settings for .vimrc and .gvimrc respectively.

Rather than moving and renaming the files I recommend creating
links to them with the following lines from the command line.

```ln -sf ~/salcode-vim-settings/vimrc.config ~/.vimrc```
```ln -sf ~/salcode-vim-settings/gvimrc.config ~/.gvimrc```

Create link to vim directory

```ln -sf ~/salcode-vim-settings/vim ~/.vim```

### Link Notes:
-f = if target already exists unlink and create new link   
-s = create a symbolic link

Shortcuts
---------
```<leader>t2``` change tab size to 2 spaces

```<leader>t4``` change tab size to 4 spaces


Author
------
Sal Ferrarello
http://twitter.com/salcode

