# About my dotfiles

My .dotfiles **ViM, DWM, zsh** and I use **ArchLinux** as my linux distribution
Mainly inspired by [ornicar](https://github.com/ornicar/dotfiles). For all my programs and shell I use [solarized
colors](http://ethanschoonover.com/solarized). There are some other scripts for convenience, like
unread gmail checks, dzen2 status bar shell script and maby other scripts which might not be needed for others at all.

## Requirements

- You will need latest **ViM** with a support of **ruby** interpreter
- **git**
- **zsh**

## Screen

![Screenshot](https://raw.github.com/l3pp4rd/dotfiles/master/screen.png)

## Installation

Clone the repository:

    clone git://github.com/l3pp4rd/dotfiles.git ~/.dotfiles

### ViM

If you do not have latest **ViM** with ruby support and all patches. You can use a shell script to install it.
**Note:** you will need GCC and all that build stuff to compile it.

    ./.dotfiles/compile/vim/build.sh

### Zsh

If you do not use **zsh** ignore the .zshrc installation, otherwise you could try to use it instead
of bash - install **zsh** first and use it as your default shell by running:

    chsh -s $(which zsh)

Install submodules

    cd ~/.dotfiles && git submodule update --init

**NOTE:** setup.sh will replace vim configs in home directory
Execute the setup script:

    ./.dotfiles/setup.sh

### Command-T

After that, for [command-t](http://github.com/wincent/Command-T) bundle you will need
to compile a **C** extension.

    cd ~/.vim/bundle/command-t/ruby/command-t
    ruby extconf.rb
    make

## Window Manager

If you are tired of bloated desktops like gnome, kde.. whatever, would recommend to try [dwm](http://dwm.suckless.org/)

**NOTE:** if you use my **~/.dotfiles/bin/startdwm** to start a window manager it most probably will not work with login
managers if you chose it as executable to run on successful login.

