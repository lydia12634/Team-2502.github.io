---
layout: post
title: Homebrew
category: Advanced
---
# What Is Homebrew?
Homebrew is

* The missing package manager for macOS it installs the stuff you need that Apple didn’t.

* Like `macports` except it isn't

* Like `apt` or `yum` if they were for macOS

* Lit AF

You will need to have agreed to the XCode TOS to be able to install homebrew.

# Installing Homebrew 

Open Terminal and execute the following command

`curl https://gist.githubusercontent.com/MDW01/ce080fa5275d646de35156ab16497de0/raw/d26f701712907eb68ed12b9f914a83c9da825477/install.rb >> install.rb && chmod +x install.rb && ./install.rb`

# Installing Homebrew Manually

[Download](https://gist.github.com/skyl/36563a5be809e54dc139) the script

Set `YOUR_HOME` in the script to `YOUR_HOME = '$HOME'`

Open Terminal and execute the following commands

`mkdir -p $HOME/usr/local`

`echo 'export PATH=$HOME/usr/local/bin:$HOME:$PATH' >> ~/.bash_profile`

`source $HOME/.bash_profile`

cd to the location of the script `cd $HOME/Downloads`

`chmod +x install.rb`

`./install.rb`

### Homebrew is now installed

[Original Source](https://gist.github.com/MDW01/ce080fa5275d646de35156ab16497de0)

[Original Source Manual](https://superuser.com/a/881681/630696)
